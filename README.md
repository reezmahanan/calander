# Simple Calendar Widget

## 📋 Overview

The **Simple Calendar Widget** is a sleek, modern monthly calendar view designed for easy embedding in any website. Built purely with HTML and CSS—**no JavaScript required**—this lightweight component offers a visually appealing way to display date information.

---

## ✨ Features

- **Pure HTML/CSS Implementation**: No JavaScript dependencies.
- **Responsive Design**: Adapts seamlessly to different screen sizes.
- **Modern UI**: Clean layout with a gradient header and subtle shadows.
- **Customizable**: Easily modify colors and styles using CSS variables.
- **Current Day Highlighting**: Visually indicates the current date.
- **Navigation Controls**: Includes styled Prev/Next month buttons and a Today shortcut (styling only).
- **Visual Distinctions**: Different styling for current, previous, and next month days.

---

## 🖥️ Preview

The calendar displays:

- Month and year in the header
- Navigation controls (styled buttons)
- Days of the week
- Days of the month with the current day highlighted
- Previous and next month days (grayed out)
- Today's date in the footer

---

## 🚀 Getting Started

### Prerequisites

- Any modern web browser
- Basic text editor for modifications

### Installation

1. **Download the HTML file**:  
   `calendar.html`
2. **Open** it in your web browser to view the calendar.

**To use in your own project:**
- Copy the entire HTML file and modify as needed.
- Extract the HTML structure and CSS styles into your existing project.

---

## 🎨 Customization

### Colors and Theme

The calendar uses CSS variables for easy customization. Modify these variables to change the color scheme:

```css
:root {
    --primary-color:    #3498db;    /* Main accent color */
    --secondary-color:  #2980b9;    /* Secondary color for gradients */
    --text-color:       #333;       /* Regular text */
    --light-text:       #777;       /* Subdued text */
    --background:       #fff;       /* Background color */
    --highlight-bg:     #f1f9ff;    /* Highlight background */
    --border-color:     #e1e1e1;    /* Border color */
    --border-radius:    10px;       /* Corner roundness */
    --shadow: 0 4px 12px rgba(0,0,0,0.1); /* Shadow effect */
}
```

### Dark Mode

A dark mode is available (commented out). To enable, uncomment and adjust as needed:

```css
/* Dark mode support
@media (prefers-color-scheme: dark) {
    :root {
        --primary-color:   #3498db;
        --secondary-color: #2980b9;
        --text-color:      #f1f1f1;
        --light-text:      #aaa;
        --background:      #222;
        --highlight-bg:    #333;
        --border-color:    #444;
    }
    body {
        background-color: #111;
    }
}
*/
```

### Changing the Month

To display a different month:

- Update the month and year in the `.month` and `.year` elements.
- Adjust the day numbers in the `.days` container for the correct month pattern.
- Update the "Today" text in the footer.

### Adding Event Indicators

To mark days with events, add the following CSS:

```css
.has-event {
    position: relative;
}
.has-event::after {
    content: '';
    position: absolute;
    bottom: 5px;
    left: 50%;
    transform: translateX(-50%);
    width: 5px;
    height: 5px;
    border-radius: 50%;
    background-color: var(--primary-color);
}
```

Then add the `has-event` class to specific day elements:

```html
<div class="day has-event">15</div>
```

---

## 💡 Implementation Notes

### HTML Structure

```plaintext
calendar-container
├── calendar-header
│   ├── month
│   └── year
├── calendar-nav
│   ├── nav-btn (previous)
│   ├── nav-btn (today)
│   └── nav-btn (next)
├── weekdays
│   └── weekday (×7)
├── days
│   ├── day prev-month
│   ├── day
│   ├── day current-day
│   └── day next-month
└── calendar-footer
```

### CSS Techniques Used

- CSS Grid for calendar layout
- Flexbox for centering and alignment
- CSS Variables for easy theming
- Linear gradients for header backgrounds
- Border-radius for rounded corners
- Box-shadow for subtle depth
- Transitions for hover effects
- Media queries (commented) for dark mode support

---

## 🔧 Making the Calendar Interactive

Currently, the calendar uses only HTML and CSS. To add interactivity:

- Add JavaScript for month navigation
- Implement date selection
- Add dynamic event handling
- Generate calendar days dynamically based on selected month

---

## 📱 Browser Compatibility

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

---

## 📝 License

This project is released under the [MIT License](LICENSE).  
Feel free to use it in personal and commercial projects.

---

## 🤝 Contributing

Contributions are welcome! Suggest improvements or create your own variations of this calendar widget.

---

## 📬 Contact

For questions or suggestions, please open an issue or reach out via [GitHub](https://github.com/reezmahanan).
