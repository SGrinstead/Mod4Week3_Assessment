# Week 3 Assessment

## Setup
* Fork and Clone this repository
* Run `update-database` - let the instructors know if you run into any issues!

## Exercise (10 Points)
### Securing the Application (4 points)
* Use Secrets Managemnt to remove the database connection string from the application.
* So that we can see the full implmentation, include a screenshot below to show your `secrets.json` file

![image](https://github.com/SGrinstead/Mod4Week3_Assessment/assets/48660896/2b136cb0-931c-4007-aa2d-80cb26ce037d)


### Maintaining Current-User (6 points)

This application includes some starter code so that we could maintain a current user.  Review the Login and Logout code in the Home Controller, along with the Login and Logout buttons in the Home/Index.cshtml file.  Building on this pre-existing structure:
* Create a cookie that holds a key for "currentUser" when a user logs in.
* Delete that cookie when a user logs out.
* Add the value of "current user" to all views

## Questions (10 Points)

For the following questions, answer as if you are in an interview!
1. Describe one strategy you have used to maintain state in a web application. (2 points)

   I maintain state in my applications by both saving information in a database and saving some smaller information in cookies. saving this information can make future visits faster and easier for the user, instead of entering new info every time they visit.

3. How would you protect sensitive data that we need to store in our database - for example, passwords? (2 points)

   I would protect sensitive data like passwords in the database by saving them as hashed data so if someone got into the database they wouldn't be able to read the data.

4. Describe 3 additional common security risks in web development. (make sure you discuss what you know about the risk, and if you know how to minimize the risk) (6 points)

   One risk is everyone having equal access to features of an api or other application. Some features like editing data should only be available to specific people. By implementing levels of authentication and authorization, we can make sure people are who they say they are and limit what they have access to.

   A second risk is someone overloading the service with a DDOS attack, and slowing or stopping service to other people. A way to prevent this is rate limiting, so a user can only make so many requests in a period of time.

   A third risk is an overposting attack, where someone will try to send a valid post request with extra information to change important data. A way to mitigate this is to use data transfer objects to put limits on what information a request can have, adding an extra layer of protection between the service layer and database.

