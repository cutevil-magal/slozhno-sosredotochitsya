# Сложно сосредоточиться — Адаптивный лендинг с системой переключения тем

**Современный адаптивный сайт с автоматическим определением системных предпочтений цвета**

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/ru/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/ru/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/ru/docs/Web/JavaScript)

---

## 📖 О проекте

Я разработала адаптивный лендинг Сложно сосредоточиться, который автоматически подстраивается под цветовые предпочтения пользователя в операционной системе. Проект демонстрирует современные подходы к веб-разработке с акцентом на доступность и пользовательский опыт.

### 🎯 Ключевые особенности

- **Автоматическое определение системной темы** через prefers-color-scheme
- **Ручное переключение тем** с сохранением выбора пользователя
- **Адаптивный дизайн** для мобильных устройств, планшетов и десктопов
- **Семантическая верстка** с использованием современных HTML5-тегов
- **CSS-переменные** для динамического управления цветовой схемой
- **Оптимизированная производительность** с lazy loading изображений

### 🛠 Технологический стек

**Frontend:**
- HTML5 (семантическая разметка)
- CSS3 (Grid, Flexbox, CSS Variables, Media Queries)
- Vanilla JavaScript (ES6+)

**Особенности реализации:**
- CSS Custom Properties для управления темами
- Методология БЭМ для именования классов
- Функция clamp() для адаптивной типографики
- Логические свойства CSS для международной поддержки
- Псевдоэлементы для декоративных элементов

---

## 🚀 Быстрый старт

### Посмотреть онлайн

🌐 **[Живая демо-версия](https://cutevil-magal.github.io/slozhno-sosredotochitsya/)**

### Запуск локально

1. **Клонирование репозитория**
   ```bash
   git clone https://github.com/cutevil-magal/slozhno-sosredotochitsya.git
   cd slozhno-sosredotochitsya
   ```

2. **Запуск проекта**
   - Откройте файл `index.html` в браузере
   - Для разработки рекомендуется использовать Live Server

### Системные требования
- Современный браузер с поддержкой CSS Variables и ES6+
- Разрешение экрана не менее 320px
- Включенный JavaScript для работы переключателя тем

---

## 📁 Структура проекта

```
slozhno-sosredotochitsya/
├── index.html              # Главная страница
├── styles/
│   ├── variables.css       # CSS-переменные
│   ├── style.css           # Основные стили
│   ├── dark.css            # Стили тёмной темы
│   ├── light.css           # Стили светлой темы
│   └── globals.css         # Общие стили тем
├── fonts/                  # Локальные шрифты
├── images/                 # Изображения
├── scripts/
│   └── script.js           # Логика переключения тем
└── README.md               # Документация
```

---

## 🎨 Особенности реализации

### Система CSS-переменных
```css
:root {
  --bg-color: #fff;
  --text-color: #353430;
  --accent-color: #ff8dcb;
  --main-font: 'IBM Plex Mono', monospace;
}

.theme-dark {
  --bg-color: #000;
  --text-color: #f1f1f1;
  --accent-color: #ff0070;
}
```

### Адаптивная типографика
```css
.title {
  font-size: clamp(7.25rem, 7.0115rem + 1.0178vw, 7.5rem);
  line-height: 82.5%;
}
```

### Семантическая разметка
```html
<header class="header">
  <nav class="header__theme-menu">
    <button class="header__theme-menu-button" data-theme="light">День</button>
    <button class="header__theme-menu-button" data-theme="auto">Авто</button>
    <button class="header__theme-menu-button" data-theme="dark">Неон</button>
  </nav>
</header>
```

### Переключатель тем
```javascript
const themeButtons = document.querySelectorAll('.header__theme-menu-button');
themeButtons.forEach(button => {
  button.addEventListener('click', () => {
    const theme = button.dataset.theme;
    document.documentElement.className = `theme-${theme}`;
    localStorage.setItem('theme', theme);
  });
});
```

---

## 🎯 Результаты реализации

**Достигнутые цели:**
- ✅ Полное соответствие макету Figma в обеих темах
- ✅ Автоматическое определение системных предпочтений
- ✅ Сохранение выбора темы пользователя в localStorage
- ✅ Адаптивность для всех типов устройств
- ✅ Оптимизированная производительность загрузки

**Технические преимущества:**
- Чистая семантическая верстка
- Использование современных CSS-технологий
- Оптимизированные медиа-запросы
- Плавные переходы между темами
- Доступность для screen readers

---

## 🔮 Планы по развитию

- [ ] Добавить PWA-функциональность
- [ ] Реализовать офлайн-режим
- [ ] Добавить дополнительные цветовые схемы
- [ ] Интегрировать систему комментариев
- [ ] Реализовать режим чтения
- [ ] Добавить анимации микро-взаимодействий

---

## 👩‍💻 Разработчик

**Анна Хвостикова** - Frontend Developer

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/cutevil-magal)
[![Email](https://img.shields.io/badge/Email-ana.magal@yandex.by-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:ana.magal@yandex.by)

---

## 📄 Лицензия

Проект создан на основе дизайн-макета. Исходный код доступен для ознакомления и обучения.
**Макет в Figma:** [Ссылка на дизайн]([https://clck.ru/3MwWDw](https://www.figma.com/design/qhgelUhPHUbJVf3jgZsaD7/3-%D1%81%D0%BF%D1%80%D0%B8%D0%BD%D1%82.-%D0%9F%D1%80%D0%BE%D0%B5%D0%BA%D1%82%D0%BD%D0%B0%D1%8F-%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0?node-id=0-1&clckid=0aee809f))

---
