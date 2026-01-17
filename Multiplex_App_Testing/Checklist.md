# **Multiplex Application Testing** #

### **Description** : Testing the Multiplex mobile app to check main functionality, UI behavior, and how the application reacts to unexpected server responses. 
Network sniffing is performed during testing. The translation vocabulary is located at the bottom of the page.
### **Environment** : Windows 10 PRO, Fiddler Classic, Android 13
### **Created by** : Igor Protsenko
### **Status** : Done
### **Version** : 1.1.1

| ID | Test Description                         | Expected result | Status |
|:---|:-----------------------------------------|:----------------|:------:|
|TC_1| Installation, deleting and reinstalation of application | Successfull instalation and reinstalion without any troubles | Pass |
|TC_2| Openning the app, closing and minimizing | Application correctly reacts on openning, closing and minimizing. App is not crashing | Pass  | 
|TC_3| Main page UI testing, testing of buttons "у кіно", "скоро", "квитки", "фільтри" and burger menu. | Correct reaction and displaying while pressing this buttons | Pass | 
|TC_4| External link following in application "Multiplex.ua" | Site Multiplex.ua opens in browser | Pass |
|TC_5| Choose some cinema theater and find available cinema sessions | Correct displaying of films with time and date of available session in choosen cinema theatre | Fail |
|TC_6| Testing of navigation to cinema theaters | Application open maps and build a route to cinema theatre | Fail | 
|TC_7| Making a call to cinema via application | Multiplex app opens phone with number and you can make a call | Fail | 
|TC_8| Create a profile in app, sign in | Succsesfull sign in and creating a profile | Pass |
|TC_9| Posibility of editing profile, changing of name, surname, email | Application receives new valus | Fail | 
|TC_10| Byuing tickets for flm session with debit card | After choosing cinema thatre, session, and places application redirects you to payment | Pass |
|TC_11| Delete profile and try to log in with old credentials | User does not exists message shown | Fail | 
|TC_12| How application layot reacts on too long long film names with symbols | UI is not broken, application is still available to use | Pass | 
|TC_13| Testing how application will handle response 500 instead of 200 | Application does not crashes, shows message with server error | Pass |
