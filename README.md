# SmartMirror
A Raspberry Pi–powered smart mirror that displays real-time time, date, weather, calendar events, and daily affirmations via a custom Python tkinter interface.
## Purpose & Motivation
This project was created to strengthen my skills in Python programming, hardware integration, and user interface design while building something practical and visually engaging.  
I wanted to explore how APIs, GUI frameworks, and embedded hardware could be combined into a seamless, always-on display.  
By focusing on a display-only design, I ensured user privacy while still delivering useful, real-time information.

---

## Technical Overview

**Hardware**
- Raspberry Pi (Model X)
- 10.1" HDMI touchscreen display
- Two-way mirror glass & custom-built frame
- MicroSD card with Raspberry Pi OS
- Power supply & HDMI connection

**Software**
- Python 3
- `tkinter` for the graphical user interface
- REST API integrations:
  - Weather API for current conditions and forecasts
  - Daily affirmation API for motivational messages
  - Calendar API for event display
- Custom Wi-Fi readiness check on boot
- LXDE autostart configuration for full-screen startup

**Key Functionality**
- Real-time clock and date display
- Weather updates at set intervals
- Daily affirmation refresh every morning
- Calendar event list with dynamic updates
- Full-screen, always-on display optimized for a 10.1" screen

---

## Challenges & Solutions

1. **Delayed Data on Boot**
   - *Challenge:* Program would launch before Wi-Fi connected, causing API calls to fail.
   - *Solution:* Added a Wi-Fi readiness check to delay startup until a stable connection was available.

2. **API Timeout & Reliability Issues**
   - *Challenge:* Occasional API request failures for weather or affirmations.
   - *Solution:* Implemented retry logic and fallback placeholder values to keep the display consistent.

5. **Autostart Reliability**
   - *Challenge:* Program didn’t always start on boot.
   - *Solution:* Adjusted LXDE autostart file with proper command order and added a delay to ensure services loaded.

---

## Future Improvements
- Expanded data modules (news, stocks, transit schedules)
- Rotate screen for portrait mode
- Build the frame for the mirror
- Install 2-way mirror
---
