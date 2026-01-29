# Multiplex Application Testing

### Description
Testing the Multiplex mobile app to verify core functionality, UI behavior, and application reaction to unexpected server responses. Network monitoring is performed during testing.  
Translation vocabulary is provided at the bottom of the page.

### Environment
- Windows 10 PRO
- Fiddler Classic
- Android 13 (Samsung Galaxy A51)

### Created by
Igor Protsenko

### Status
Done

### Version
1.1.1

| ID    | Test Description                                                                 | Expected Result                                                                  | Status |
|-------|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|:------:|
| TC_1  | Install, delete, and reinstall the application                                  | Application installs and reinstalls successfully without issues                | Pass   |
| TC_2  | Open the app, close it, and minimize it                                          | The app opens, closes, and minimizes correctly. App does not crash             | Pass   |
| TC_3  | Main page UI testing: tabs “у кіно”, “скоро”, “квитки”, Filters button, burger menu | Buttons respond correctly and screens display as expected                      | Pass   |
| TC_4  | Follow an external link in the application (“Multiplex.ua”)                      | The Multiplex.ua website opens in the browser                                   | Pass   |
| TC_5  | Choose a cinema theatre and view available cinema sessions                  | Available films in choosen cinema theatre, with time and dates, are displayed correctly         | Fail   |
| TC_6  | Test navigation to cinema theaters.                                              | The app opens maps and displays route to the cinema                             | Fail   |
| TC_7  | Make a call to the cinema from the application. Network sniffing                 | The phone app opens with the number ready to dial                               | Fail   |
| TC_8  | Create a profile and sign in                                                     | Profile is created and user can log in                                          | Pass  |
| TC_9  | Edit profile (change name, surname, email)                                       | Application updates profile fields correctly                                    | Blocker |
| TC_10 | How aplication reacts to high latency                                            | Application shows message “Request timed out. Please try again.”                | Pass   |
| TC_11 | Try to log in with wrong OTP code                                                | “Wrong code” message is shown                                                    | Pass   |
| TC_12 | Long film name UI behavior                                                       | UI does not break; the application is still usable                              | Pass   |
| TC_13 | Simulate server response 500 instead of 200                                      | The app does not crash and shows a server error message                         | Pass   |

---

### Vocabulary
- **у кіно** – *in the cinema*  
- **скоро** – *soon*  
- **квитки** – *tickets*  
- **фільтри** – *Filters*
