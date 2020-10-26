# ImageHoster

This project is an assignment to fulfil the Post Graduate Diploma in Fullstack development from IITB and Upgrad. There are two parts of the Assignment 

Part A: Fixing Issues
1. Image upload issues:

If you upload an image with the same exact title as of a previously uploaded image, it will get uploaded. But then, if you try to navigate to one of the images with the same title, the image uploader will display an error.
Please fix this issue, so that the application should not show an error and take you to respective image’s page.
Please see more details of this issue on Github.
 

2. After logging into the application, it is possible to edit/delete the image which is posted by some other user. This is a bug in the application. Now, fix this bug in the application, such that only the owner of the image can edit/delete the image. Check this link for more details.

If the owner of the image is trying to edit the image, you must return the ‘images/edit.html’ file, thus enabling the user to edit the image. But if the non-owner of the image is trying to edit the image, return the ‘images/image.html’ file displaying all the details of the image and print the message ‘Only the owner of the image can edit the image’. Carefully add all the required attributes in the Model type object needed by ‘images/image.html’ file.

Part B: Implement a new feature
After fixing the above issues, please implement the following features into the image uploader application:

1.  Password Strength

Up till now, there is no check on the strength of the password entered by the user at the time of registration. Let us try to keep a check on the strength of the password entered by the user at the time of registration. You need to implement a feature wherein the password entered by the user must contain at least 1 alphabet (a-z or A-Z), 1 number (0-9) and 1 special character (any character other than a-z, A-Z and 0-9). The user must only be registered if the password contains 1 alphabet, 1 number, and 1 special character. And after successful registration, you must directly return 'users/login.html' file. Otherwise, the user must not be registered and again return the ‘users/registration.html’ file. You also need to display a message ‘Password must contain at least 1 alphabet, 1 number & 1 special character’. Carefully add all the required attributes in the Model type object needed by ‘users/registration.html’ file.
Observe the registration web page and the password does not contain any number or special character.

2.  Comments

Now, implement a feature wherein a user can add a comment to any image in the application after he is logged in the application, and, to implement this feature, you’ll have to add the following to the image uploader application:

Create a Comment model class. The model class contains the following attributes:
id - Datatype should be int. It should be a primary key. Also explicitly mention the column name as ‘id’ to be created in the database.
text - Datatype should be a string. Note that this column can have text-based data that will be longer than 256 characters.
createdDate - Datatype should be LocalDate.
user - It should be of type User. The ‘comment’ table is mapped to ‘users’ table through this attribute. One user can post multiple comments but one comment should belong to one user. Write the suitable annotation to map the ‘comment’ table to ‘users’ table through this attribute.
Image - It should be of type Image. The ‘comment’ table is mapped to ‘images’ table through this attribute. One image can have multiple comments but one comment can only belong to one image. Write the suitable annotation to map the ‘comment’ table to ‘images’ table through this attribute.
