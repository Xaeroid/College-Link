# College-Link
This project is aimed at increasing competitiveness among students(preferably students of a specific college) by creating a platform for connecting, conversing and competing in various events held worldwide.

College - Link is an android application wherein college students can register, create their profiles, add their skills, connect to other students of various fields and expand their network meanwhile forming a perfect team for their next competition! Being unaware of any upcoming event is out of the question now!

Main features of the application :
Register/login using your email id and password.

Add your skills.

Add a post along with the skills associated with it.

View your feed, where your post and other users' post will be displayed.

Get notified when a post is added which matches your skill(s).

Like other users' posts.

Comment on other users' posts.

Chat with other users.

View the list of all registered users.

View other users' profiles.

Block/unblock any user.

Side features of the application :

Edit your skills, name, email, password and profile picture.

View the number of likes and comments on every post.

See a list of all users who liked a certain post.

View all comments on every post.

Search for a particular post on the homepage using words from its title or description.

Search for a particular user on the users page by their name or any corresponding alphabets from their name.

Go to the chat screen directly from any user's post.

See the last seen of any user you're chatting to.

Visualizing the project :

We've made a video showcasing the application and explaining how it actually works. Watch the video here.

This project has been listed on Devfolio. View it here.

We made a presentation before actually creating the application which served as a guidance tool. View that presentation here.

Download the APK file :

We are currently in progress for publishing the app on Playstore so it's not available there yet.

On the right-hand side of this repository, you'll find the latest release of this application. You can download the apk file as well as the source code for this app by clicking 
on that tag.

You can download and install the apk file on your android device from here as well.

How to test this application on your own system :

First of all, make sure you have Git installed in your system. Open CMD and paste - git clone https://github.com/Hacks-On/CollegeLink.



Now, open Android Studio and open the cloned project.



Let the gradle sync/build(some dependencies and SDKs will be downloaded and installed). Meanwhile, go to Tools>Firebase and select :



Authentication>Authentication using a custom authentication system. Connect your app to Firebase and add the FirebaseAuth SDKs to your project.



Realtime Database>Get started with Realtime Database. Add the FirebaseDatabase SDKs to your project.



Cloud Storage for Firebase>Get started with Cloud Storage. Add the FirebaseStorage SDKs to your project.



Please note that the above step helps you connect the cloned project to your own Firebase project on the Firebase console. You can skip this step since the application is 
already connected to our Firebase project and the dependencies for the SDKs are already present in the gradle files(which are being installed during gradle sync/build).
Once the gradle finishes building, you're good to go. Connect Android Studio to your android device or create a virtual device using the AVD manager. Now, run the app. Voila!
If you encounter any bugs while using the application or want to suggest any improvements/features, feel free to create an issue for the same and we'll look into it!

External services/libraries used :
Firebase Authentication(implementation 'com.google.firebase:firebase-auth:19.0.0') : This Firebase service helps in authenticating the users and logging them it/out. It currently being done using email and password.Firebase Realtime Database(implementation 'com.google.firebase:firebase-database:19.0.0') : This Firebase service forms almost the complete back-end of this application. Almost all the data being fetched in the application is stored and retreived using this database only.
Firebase Storage(implementation 'com.google.firebase:firebase-storage:19.0.0') : To upload images or any graphical content, we need a storage unit apart from the database for these items. This task is accomplished using Firebase Storage wherein all the images uploaded by the user(post images and profile pictures) are stored.
Volley library(implementation 'com.android.volley:volley:1.1.1') : This is an HTTP library aimed at making networking for android apps much more easier and faster.
Circle Image View(implementation 'de.hdodenhof:circleimageview:3.1.0') : This library is used to display any image inside a circular container/frame.
Gson library(implementation 'com.google.code.gson:gson:2.8.6') : This library is aimed at converting JSON strings into their corresponding Java objects and vice-versa.
Concepts used :
Authentication : For any social media application wherein multiple users can connect to each other, authentication is a must. Else, the application may be used in ways it's not supposed to be used. Therefore, we have used FirebaseAuth service for authenticating the users.
DBMS : The complete backend of this application is dependent on a cloud-hosted database known as Firebase. Databases are powerful tools which help us store data of various types in an organized way. Firebase offers a lot of features for easy manipulation of the database using Android Studio.
Fragmentation : Instead of using different activities for different functions of the application, we have used fragments.
Model classes : Model classes contain getters and setters for the variables defined in them. These are used in the corresponding Adapter classes/other classes.
Adapter classes : Adapter classes are a link between the front-end and the back-end of the application. They are responsible for transferring data between multiple classes and displaying it as per requirement.
Java files created :
SplashScreenActivity.java : Responsible for displaying a splash screen everytime the user opens the application.

MainActivity.java : Contains the code for creation of different fragments and the route to each of them.

RegisterActivity.java : Responsible for registering a new user using their email and password or redirecting an existing user to the login page.

LoginActivity.java : Responsible for authenticating an existing user and logging them in or redirecting them to the register page.

SkillPage.java : Displays various checkboxes for the user to select their relevant skills and uploads the selection in the database.

ModelChat.java : Contains getters and setters for retrieving/assigning values to various variables required to allow chat functionality between two users.

AdapterChat.java : Contains various functions to transfer data between chat classes and display it using whichever view required.

ChatActivity.java : Responsible for showing the chat screen between two users and performing various functions around it.

ModelChatlist.java : Contains getters and setters for retrieving/assigning values to various variables required to allow displaying all the chats of the current user.

AdapterChatList.java : Contains various functions to transfer data between chatlist classes and display it using whichever view required.

ChatboxFragment.java : Responsible for displaying all the chats of the current user as received from the chatlist classes.

ModelUsers.java : Contains getters and setters for retrieving/assigning values to various variables required to allow displaying a list of registered users.

AdapterUsers.java : Contains various functions to transfer data between user classes and display it using whichever view required.

UsersFragment.java : Responsible for displaying all the registered users as received from other user classes.

ModelPost.java : Contains getters and setters for retrieving/assigning values to various variables required to allow displaying all available posts on the homepage and other functionalities.

AdapterPosts.java : Contains various functions to transfer data between post classes and display it using whichever view required.

HomeFragment.java : Responsible for displaying all the available posts with various functionalities.

PostDetailsActivity.java : Responsible for displaying the details of any post which the user clicks on.

PostLikedByActivity.java : Responsible for displaying a list of all the users who liked a certain post.

AddpostFragment.java : Allows taking inputs from the user in various fields and adds all the details in the database for further usage.

ModelNotifications.java : Contains getters and setters for retrieving/assigning values to various variables required to allow displaying notifications to every user.

AdapterNotifications.java : Contains various functions to transfer data between notification classes and display it using whichever view required.

NotificationsActivity.java : Responsible for notifying a user regarding publishing of a post which matches the user's skills. It displays a list of all such notifications.

ProfileFragment.java : Responsible for displaying the details of the current user and allowing them to edit their name, email, profile picture_ and skills.

EditProfilePage.java : Allows the user to edit their details - name, email and profile picture, same would be updated in the database.

ProfileSkillPage.java : Allows the user to update their skills, same would be updated in the database.

TheirProfileActivity.java : Reposible for displaying the details of any user selected from the user's list.

ModelComment.java : Contains getters and setters for retrieving/assigning values to various variables required to allow users to comment on the posts published by other users.

AdapterComment.java : Contains various functions to transfer data between comment classes/other classes and display it using whichever view required.

Sender.java : Contains getters and setters for misc. functions related to chat and notifications.

Data.java : Contains getters and setters for misc. functions related to chat and notifications.

Token.java : Contains getters and setters for misc. functions related to chat and notifications.

UserHelper.java : Contains getters and setters for helping the user register/login. This file is currently not in use.

Extra XML files created :
Whenever an Activity or Fragment is created, an XML file is also created along with it which defines the design and UI elements of that activity/fragment. But, apart from those files, we have created some extra XML files as well :

row_chat_left.xml : Contains the design for displaying the messages of the second person in the chat.

row_chat_right.xml : Contains the design for displaying the messages of the first person(the current user) in the chat.

row_chatlist.xml : Contains the design of a dummy chatlist as it will be displayed in the chatbox fragment.

row_posts.xml : Contains the design of a dummy post as it will be displayed on the user's feed.

row_notifications.xml : Contains the design of a dummy notification as it will be displayed on the notifications screen.

row_users.xml : Contains the design of a dummy user as it will be displayed in the users fragment.

row_comments.xml : Contains the design of a dummy comment as it will be displayed on any post.

dialog_update_password.xml : Contains the design for the dialog box which pops up when the button for changing password is clicked.

Please note :

First of all, connect your app to Firebase. Then, add the required Firebase SDKs for the Firebase services being used in the app(FirebaseAuth, FirebaseDatabase, 
FirebaseStorage). This can be done either by adding the required dependencies manually(these can be found at Firebase Documentation) in the gradle files which will download the 
SDKs, or by using the IDE to add the SDKs automatically(go to Tools>Firebase to do so).

Update AndroidManifest.xml file as per the one present in this repository. Do note that all the activities present in the project are mentioned in this file.

Update app>src>main>res>drawable folder. This folder contains the xml files used.

Update app>src>main>res>font folder. This folder contains the external fonts used.

Update res>values>colors.xml file. This folder contains the external colors used.

Update res>values>strings.xml file. This folder contains the external strings used.

Future enhancements :

Making different database segments for different colleges and assigning a unique key to students of a particular college. This way, this app can be uniquely used by each college 
throughout the world. Although, to implement this, a strong and huge database will be required. Luckily, Firebase itself offers such a service(paid) which can make this 
application production-ready.
Adding the feature to create a group by selecting certain users and starting a group chat.
Adding voice chat/meet feature.
Adding the feature to add videos and links in your posts as well.
Creating drop-down menus for adding a lot more skills from every tech-domain.
Extending the app to non-tech fields as well. A seperate space can be created for users interested in these fields and same functionalities can be implemented in that space as well.
UI/UX improvements to match the modern trends of social media.
Improving the accessibility of posts, users and notifications and making them more detailed.
