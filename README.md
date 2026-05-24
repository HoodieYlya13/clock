# 🕰️ Real-Time Analog & Digital Clock

A highly-polished, responsive timepiece application combining a traditional analog clock face with a real-time digital readout. Using modern CSS transforms and native JavaScript date calculation APIs, this project provides a fluid, high-fidelity experience with zero dependencies.

---

## ✨ Features

*   **🕒 Hybrid Visuals:** Combines a fluid, ticking analog clock interface with a modern 24-hour digital timestamp.
*   **🔄 Smooth 3D Sweeps:** Analog clock hands dynamically rotate based on accurate math mapping, converting the system time into rotational degrees.
*   **🎨 Premium Typography:** Styled using the premium monospace font family **JetBrains Mono** via Google Fonts, ensuring crisp, modern alignment.
*   **📱 Responsive & Fluid Layout:** Adapts seamlessly to various screen dimensions and layouts with flexible viewport-based units.
*   **🏷️ Custom Branding:** Features a integrated header badge pointing back to **[HY13dev](https://www.hy13dev.com/)**.

---

## 🛠️ Architecture & Under the Hood

The project utilizes precise physical ratios to avoid jerky movements on minute/hour transitions:

*   **Seconds Ratio:** `currentSeconds / 60`
*   **Minutes Ratio:** `(secondsRatio + currentMinutes) / 60`
*   **Hours Ratio:** `(minutesRatio + currentHours) / 12`

This allows the hour and minute hands to gradually and realistically drift forward as the seconds progress, rather than jumping abruptly each minute. Hand rotations are updated once every second (`1000ms`) using:

```javascript
element.style.transform = `rotate(${rotationRatio * 360}deg)`;
```

---

## 💡 Installation & Launch

### 1. Clone the repository
```bash
git clone https://github.com/HoodieYlya13/clock.git
cd clock
```

### 2. Run the application
Open `src/index.html` directly in any web browser, or spin up a local development server:
```bash
npx serve .
```

---

## 👨‍💻 Developer

Built with ❤️ by **[Ylya Martchenko (HY13dev)](https://www.hy13dev.com/)**.
