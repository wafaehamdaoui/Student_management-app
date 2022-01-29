# Student_management-app
this is my final project of GUI Programming with QT course

## School Management System

School Management System is a large database system which can be used for store student's information. Most importantly, this information can be easily shared with authorized users, records can be easily searched, and reports can be easily generated.

The application that I created is a simple interface where you can store personnals informations of students and thier courses.

So my application allo you to register students as an `administrator_login` and allow you to do some operations on those records like ***Search***, ***Update*** , ***Delete***... or you can just view your own information as a `student_login` .

**In my project I respect the following points:**

> I used QMainWindow,

> I used MCV model ,

> I used the concept of signals && slots ( ***connection*** ),

> I used Layouts,

> And of caurse to set a style I used css .

> I try to have an app that provides us with a sevice (store ,search, update, delete ...),

**This is what it’ll look like at the end of this project**

![image](https://user-images.githubusercontent.com/75392302/151638461-100993ed-26f6-4a0d-916f-6dd4d6d9163f.png)

### Resource Files
School management systeme uses several icons to represent various actions. The icons are in the resources directory which is directly under the project directory.

To register the image files, in the Edit mode, right-click the icons.qrc file and select Open in Editor.

Click the Add button and select Add Files.

In the file manager, select the files to be added.

### Resource Classes

> **QMainwindow** ,
 
> **QDialog** , 

> **QLayout** , 

> **QLabel** , 

> **QPixmap** ,

> **QSqlDatabase** ,
   
> **QSqlQuery** ,

> **QMessageBox** , 

> **QCoreApplication** , 

> **QtDebug** , 

> **QSqlDriver** ,

> **QSpacerItem** 


Mainly our application is devided in to part , one take care of students users ant the other one  focus on Admins users .

## Part One:

 School management Application is in the MainWindow class, which inherits QMainWindow. QMainWindow provides the framework for windows that have menus, toolbars, dock windows, and a status bar. 
 
 The application provides File, Tools, View and Help entries in the menu bar, with the following Actions:
 
 
 
 
 
 
 
