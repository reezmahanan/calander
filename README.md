# 📅 Simple Calendar Widget

A sleek, modern monthly calendar built with pure **HTML & CSS**—no JavaScript required!  
Perfect for easy embedding in any website, blog, dashboard, or project.  
Lightweight, responsive, and fully customizable.

---

## 🚀 Live Demo

**Try it live:**  
[Simple Calendar Widget Demo](https://reezmahanan.github.io/calander/)

---

## 🖼️ Screenshot

![Calendar Widget Screenshot](https://github.com/reezmahanan/calander/blob/main/Screenshot%202025-09-14%20112604.png)

---

## 📋 Overview

The **Simple Calendar Widget** offers a visually appealing monthly view with intuitive layout, stylish navigation controls, and clear date highlighting—all powered by smart CSS.  
Just open the HTML file and enjoy a beautiful calendar, or easily drop it into your own project!

---

## ✨ Features

- **Pure HTML/CSS Implementation**: No JavaScript needed.
- **Responsive Design**: Looks great on desktop and mobile.
- **Modern UI**: Gradient header, rounded corners, smooth shadows.
- **Customizable**: Tweak colors and styles with easy CSS variables.
- **Current Day Highlighting**: Instantly see today’s date.
- **Navigation Controls**: Styled Prev/Next month and Today shortcut buttons (styling only).
- **Visual Distinctions**: Different styles for current, previous, and next month days.
- **Dark Mode Ready**: Commented CSS template for easy dark theme.

---

## 🖥️ Preview

The calendar displays:

- **Month & Year** in the header
- **Navigation Controls** (styled buttons)
- **Days of the Week**
- **Month Days** with current day highlighted
- **Previous/Next Month Days** (grayed out)
- **Today's Date** in the footer

---

## 🛠️ Getting Started

### Prerequisites

- Any modern web browser
- Text editor for optional customization

### Installation

1. **Download** `calendar.html`
2. **Open** in your browser to view the calendar

**To embed in your own project:**  
Copy the HTML & CSS into your site and adjust as you wish!

---

## 🎨 Customization

### Colors & Theme

Update the CSS variables at the top of the stylesheet for instant restyling:

```css
:root {
    --primary-color:    #3498db;
    --secondary-color:  #2980b9;
    --text-color:       #333;
    --light-text:       #777;
    --background:       #fff;
    --highlight-bg:     #f1f9ff;
    --border-color:     #e1e1e1;
    --border-radius:    10px;
    --shadow: 0 4px 12px rgba(0,0,0,0.1);
}
```

#### Dark Mode

Enable dark mode by uncommenting and tweaking:

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

### Change the Month

- Update `.month` and `.year` elements in the header
- Change day numbers in `.days` container
- Update footer “Today” text

### Add Event Indicators

Add a dot to mark event days:

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

Then in HTML:

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
│   ├── nav-btn (prev)
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
- Flexbox for alignment
- CSS Variables for easy theming
- Linear gradients for header
- Border-radius for rounded corners
- Box-shadow for depth
- Transitions for hover effects
- Media queries (commented) for dark mode

---

## 🔧 Making the Calendar Interactive

Want navigation, date selection, or event popups?  
Just add JavaScript to:

- Change months dynamically
- Select dates
- Manage events
- Auto-generate days for each month

---

## 📱 Browser Compatibility

- Chrome, Firefox, Safari, Edge (latest)
- Mobile browsers

---

## 📝 License

Open source & free under the [MIT License](LICENSE).

---

## 🤝 Contributing

Your ideas, improvements, and variations are welcome!  
Fork the repo, submit PRs, or just leave your compliments ⭐

---

**If you like this calendar, please give it a star!**  
Made with 💙 by [reezmahanan](https://github.com/reezmahanan)
