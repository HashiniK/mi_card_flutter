# artgalaxy-mobile

Root directory of the project **Art Galaxy**. This project is only implemented for **Android** and have used the **Flutter framework** for implementation.

## artgalaxy-mobile
This is the directory that contains all the related files and directroies.

>**artgalaxy-mobile**
>>...
>>assets
>>>datasource
>>>fonts
>>>images
>>>translations
>>>>en-US.json
>
>>config (package)
>>>>lib
>>>>>config.dart
>
>>lib
>>>dao
>>>>base_dao.dart
>>>>db.dart
>>>>post_dao.dart
>
>>>helper
>>>>aws_download_util.dart
>>>>aws_upload_util.dart
>>>>constants.dart
>>>>gql_service.dart
>>>>image_cache.dart
>>>>image_preview.dart
>>>>theme.dart
>>>>uploader.dart
>>>>util.dart
>>>>video_capture_controller.dart
>
>>>model
>>>>common.dart
>>>>gql_login.dart
>>>>gql_media.dart
>>>>gql_post.dart
>>>>gql_recovery.dart
>>>>gql_registration.dart
>>>>gql_resources.dart
>
>>>ui
>
>>>>account
>>>>>change_password.dart
>>>>>disclaimer.dart
>>>>>edit_profile.dart
>>>>>forget_password.dart
>>>>>login.dart
>>>>>signup.dart
>>>>>verify.dart
>
>>>>components
>>>>dashboard
>>>>>dashboard.dart
>
>>>>mygallery
>>>>>my_gallery.dart
>>>>>my_gallery_actions.dart
>>>>>my_gallery_basic.dart
>>>>>my_gallery_images.dart
>>>>>my_gallery_info.dart
>>>>>my_gallery_profile.dart
>>>>>my_gallery_shop.dart
>>>>>my_gallery_stats.dart
>
>>>>post
>>>>>create_post.dart
>>>>>view_post.dart
>
>>>>app_theme.dart
>>>>file_util_theme_data.dart
>>>>launcher.dart
>>>>navigator.dart

>>>main.dart
>
>>pubspec.yaml
>>README.md

### assets
This will be used to store static images, translation files, custom fonts and datasources. The asset paths will be included in the **pubspec.yaml** file so that flutter can recognize where the assets are present.

 * #### fonts
This contains all the custom fonts that has been used throughout the application. 
 * #### images
This contains all the static images that have been used throughout the application. 
 * #### translations
This contains all the translation files that can be used to translate the widget texts that are visible to the user. The translation files are in **.json** extension.

> - **en-US.json** - contains the localization keywords that have been used throughout the application  

### lib
The lib folder contains the UI related folders. 

#### dao
This directory contains all the **.dart** files that establishes the database connectivity. 

> - **base_dao.dart** - This is  the super class which will be inherited by all the custom created child classes (post_dao.dart).
>
> - **db.dart** -This is the database connectivity manager. 
> 
> - **post_dao.dart** - This is where the direct database manipulation will be handled related to posts. 

#### helper
This directory contains all the **.dart** files containing wrappers, and widgets that are used constantly throughout the application. 
>- **aws_download_util.dart** 
>- **aws_upload_util.dart**
>- **constants.dart**
>- **gql_service.dart**
>- **image_cache.dart**
>- **image_preview.dart**
>- **navigation_controller.dart**
>- **theme.dart**
>- **uploader.dart**
>- **util.dart**
>- **video_capture_controller.dart**

#### model
Contains the data models which will be used throughout the application. These models will be imported by other classes. 

#### ui
This folder contains all the sub folders which includes all the **.dart** files which implements the complete UI of the application. 

* #### account
 
This directory contains all the files related to the user such as change password, disclaimer, edit profile, forget password, login, signup, and verify. 

> - **change_password.dart** - This is where the API request is made to set the password. The user can get to hear from,
>> - Login ---> Forgot Password ---> Verify OTP ---> Set Password

> - **disclaimer.dart** - This is where the UI is implemented for the terms and policies of the application. The user can get to hear only through Sign Up during the sign up process. 

> - **edit_profile.dart** - This is where the API request is made to change the user's details such as the username, bio, website URL, and email address. The user can get to hear from,
	>> - My Gallery ---> Edit Profile

> - **forget_password.dart** - This is where the API request is made to request the OTP, when the user clicks on the Forgot Password button in the Login Page.  The user can get to hear from,  
>> - Login ---> Foget Password 

> - **login.dart** - This is where the API request is made when the user logs in. The user can get to hear from the landing page which shows the button to log in. The user's email, password will be passed and once they are verified, the user will be redirected to the Dashboard. 

> - **signup.dart** - This where the user sign ups. The API request will be sent with the user's typed data such as username, email address, password, and their birth date.The user can get to hear from the landing page which shows the button to sign up. 

> - **verify.dart** - This is where the API request is made when the user needs to verify their new account, set a new password, request another OTP to set a new password or to verify their account. The user can get to here from two ways, 
>> - Sign Up ---> Verify OTP
>> - Forget Password ---> Verify OTP

 * #### components
 
This directory contains all the components that contains the basic UIs which has been imported by other classes.  

 * #### dashboard

This contains the file that implements the UI of the dashboard of the application. 

* #### mygallery

My gallery is the directory which contains all the files that are related to the user's gallery. The gallery is where all the user's shared posts, actions, basic information, stats, info, profile and shop. The main file that connects all the other sub folders is the **my_gallery.dart** file. This builds the complete view of the my gallery. 

* #### post

This is the directory which contains all the UI related files when a user shares and views a post. The two files inside this folder are **create_post.dart** and **view_post.dart**.






### pubspecs.yaml
This is the file the contains the metadata and configuration specific to our application. This is used to configure dependencies such as image assets, fonts, and app versions.

