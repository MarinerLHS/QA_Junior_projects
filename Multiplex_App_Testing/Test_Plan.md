# Multiplex Application Test Plan

## 1. Introduction
- The purpose of this test plan is to define the scope, objectives, and test resources for testing the Multiplex mobile application.
- The goal of testing is to verify that the main functionality of the application works correctly.
- Testing covers UI behavior, localization correctness, navigation to cinemas, installation, uninstallation, and application updates.
- Network behavior is tested to verify how the application reacts to different server responses.
- The application interface is in Ukrainian. English translations are provided inside test cases where required.

---

## 2. Test Objectives
- Verify installation, registration, login, and profile information management.
- Validate UI behavior during user interactions such as swiping, navigation, and button usage (Filters, Overview, Burger Menu, etc.).
- Verify correctness of navigation, localization, and the ability to contact cinemas.
- Verify handling of external links (e.g., Google Maps, phone calls).
- Verify application behavior under unexpected or false network responses.

---

## 3. Scope

### In Scope
- Mobile UI and functional flows
- Network error handling
- User actions: registration, login, profile editing, ticket reservation
- Installation and uninstallation

### Out of Scope
- Test automation
- Performance and load testing

---

## 4. Test Approach
- Manual functional and non-functional testing.
- Smoke testing to validate basic application stability.
- Exploratory testing to evaluate usability and general behavior.
- Negative and network testing using Fiddler to simulate unexpected server responses and observe UI behavior.

---

## 5. Test Types
- **Smoke Testing**: Installation/uninstallation, application launch, main screen validation.
- **Exploratory Testing**: Free navigation through the application, swiping, filtering, and interaction with UI elements.
- **UI Testing**: Layout, buttons, tabs, icons, and text visibility.
- **Network Testing**: Handling of server errors (e.g., 404, 500), malformed responses.
- **Negative Testing**: Invalid input data, login attempts with deleted accounts.

---

## 6. Test Environment
- Mobile Device: Samsung Galaxy A51, Android 13
- Optional Device: iPhone (iOS)
- PC: Windows 10 or higher
- Tools: Fiddler Classic
- Network: Wi-Fi
- External Services: Google Maps, Chrome browser

---

## 7. Entry Criteria
- PC and Android mobile device are available.
- Fiddler is installed on the PC.
- Proxy is configured on the PC.
- Mobile device is configured for proxy usage and required certificates are installed.
- Stable Wi-Fi connection is available.

---

## 8. Exit Criteria
- All planned test cases are executed.
- Test documentation and screenshots are prepared.
- All identified defects are documented and reported.

---

## 9. Risks
- Possible differences in application behavior on iOS.
- Language barrier due to Ukrainian-only interface.
