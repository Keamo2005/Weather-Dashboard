# Weather Dashboard
- **Developer**: Keamo Seloane
- **Student Number**: ST10528238
- **Group**: 3
- **Course**: Higher Certificate in Mobile Application and Web Development
- **Subject**: MAST

## Links
- **GitHub Repository**: https://github.com/Keamo2005/Weather-Dashboard

---

## Project Overview

The **Weather Dashboard** is a app developed as part of an assignment in the MAST subject. This application was created using **Kotlin** and **Visual Studio**. The app's primary purpose is a weather dashboard.

The **Weather Dashboard** application is a dynamic, multi-city mobile interface built with React Native. It displays a collection of environmental metrics for three major South African cities: Johannesburg, Cape Town, and Durban. The application provides users with an overview of current weather parameters (including temperature, perceived "feels like" metrics, wind dynamics, visibility, and barometric pressure), followed by a 24-hour horizontal forecast array and a 5-day future list.

---

## Development Environment

The application was debugged, optimized, and tested using the following software stack and configurations:
- Expo
- React Native
- TypeScript
- Institutional VM (Virtual Machine Environment)
-  BlueStacks 5 (Android Development Virtualization)
-  Expo Go

---

## Error Log

Below is the breakdown of the syntax issues, component bugs, and logic errors discovered in the original codebase, along with explaining what was wrong and how it was corrected:

- <ImageBackground> | Missing Import | Added `ImageBackground` to the `react-native` import statement.
- `weather.country` instead of `weather.city`, | Logic Error | Updated the state matching to `weather.city`.
- The background image source | Property Formatting | Wrapped the string inside an explicit URI object structure: `source={{ uri: ... }}`.
- The Humidity section displayed the `feelsLike` | Data Error | Corrected the text string variable name to target `${selectedWeather.humidity}%`.
- The 24-Hour Forecast `ScrollView` layout was set to `horizontal={false}` | Layout Error | Reconfigured the scrolling orientation layout attribute to `horizontal={true}`.
- The hourly forecast map showed `selectedWeather.temperature` | Loop Error | Swapped the data binding reference to `{hour.temperature}°`.
- The 5-Day Forecast rows inverted in the wrong order | Display Logic Error | Rearranged the variables to `{day.high}°` followed by `{day.low}°`.
- The "Sunrise" custom data row called the `sunset` | Data Mismatch | Corrected the declaration to `selectedWeather.sunrise`.

---

## GitHub and GitHub Actions

This project was managed using **GitHub** for version control, where all code changes were committed and pushed regularly. GitHub enabled collaborative coding, allowing me to keep track of changes and maintain project integrity.

### GitHub Actions:
I utilized **GitHub Actions** to automate the build and deployment process. This includes:

- Running automated **tests** to ensure the appâ€™s functionality.
- Compiling the app into **APK** and **AAB** files, which are the formats required for distribution.
- Uploading these build artifacts to GitHub for easy access.

The workflow ensures that my project is automatically built and tested every time I push changes, and it simplifies the process of delivering the final APK/AAB files for submission.

---

## 4. Testing

The corrected application bundle was evaluated inside the BlueStacks 5 emulator runtime via the Expo Go application:

* **Multi-City Testing:** Interactively clicked through the Johannesburg, Cape Town, and Durban selector buttons. Confirmed that active tabs updated theme colors cleanly and that the global dashboard successfully swapped data matrices without memory stalls.
* **Swipe Testing:** Mouse-drag swipe interactions across the 24-Hour Forecast array.

* **Error** Emojis are cropped out.
---

### App Screenshots:

<img width="540" height="960" alt="Screenshot_2026 10 08_20 06 08 122" src="https://github.com/user-attachments/assets/ad26a3f5-8d16-47e5-bda3-fc754a4f9641" />

<img width="540" height="960" alt="Screenshot_2026 10 08_20 07 07 944" src="https://github.com/user-attachments/assets/832b173c-6d04-4e9c-8e55-bd1dd173415e" />

<img width="540" height="960" alt="Screenshot_2026 10 08_20 07 21 651" src="https://github.com/user-attachments/assets/6f64fe9c-b0a6-4c0e-b6e3-aeb9ccd9d6c7" />

---

## 6. Conclusion
Investigating and refactoring the broken Weather Dashboard code provided key insights into the layout constraints of React Native text rendering, type structures, and framework component states. 
Resolving the terminal crashes emphasized that React Native enforces a strict validation rule: no text strings or stray characters may exist outside a `<Text>` component container boundary. Furthermore, adjusting the 5-Day Forecast loop maps clarified the syntax difference between component returns using parentheses `()` versus statement blocks using curly braces `{}`. 
Ultimately, this task demonstrated the importance of development terminal logs to isolate syntax issues and implement target style buffers when deploying applications to mobile emulators.

---

## References

Jessel Sookha - Weather Dashboard coding
