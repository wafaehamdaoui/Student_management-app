# School_management-app
this is my final project of GUI Programming with QT course

## Acknowledgement:

I want to thank Allah for helping me to complete this work in every single step.

It is an honor for me to thank my advisor. This would not be possible without his help and support.

## Introduction

School Management System is a large database system which can be used for store student's information. Most importantly, this information can be easily shared with authorized users, records can be easily searched, and reports can be easily generated.

## Motivation:

▪ To meet a solution to manage students' records .

▪ To overcome existing problems occurring in maintenance of students' information.

## Objectives:

▪ To manage students' information guring admission and examination.

▪ Efficient utilization of human resource.

▪ To reduce unnecessary paper work in maintaining students' information.

## Applications:

▪ To use for various streams' student.

▪ To gather students' information.

▪ Different reports and queries can be generated based of vast options related to students ,courses, Teachers...

## Data Flow Diagram of SMS :

![image](https://user-images.githubusercontent.com/75392302/152677987-ef3147e4-de03-4e40-b29c-a22f80e4dc57.png)
![image](https://user-images.githubusercontent.com/75392302/152678240-2a8b6efe-a2d2-4e56-bf2b-317013d69620.png)
![image](https://user-images.githubusercontent.com/75392302/152678304-3a2b616a-3b19-4585-91b6-7cc8bfcdf642.png)



**In my project I respect the following points:**

> I used QMainWindow,

> I used MCV model ,

> I used the concept of signals && slots ( ***connection*** ),

> I used Layouts,

> And of caurse to set a style I used css .

> I try to have an app that provides us with a sevice (store ,search, update, delete ...).

**This is what it’ll look like at the end of this project**

![image](https://user-images.githubusercontent.com/75392302/152678477-582b84a1-1312-4baf-8d4b-f73d4e784b57.png)

-> Mainly our application is devided in to Three part , one take care of students users , the other one  focus on Teachers users and the last one is about Admins users .

### Resource Files
School management systeme uses several icons to represent various actions. The icons are in the resources directory which is directly under the project directory.

To register the image files, in the Edit mode, right-click the icons.qrc file and select Open in Editor.

Click the Add button and select Add Files.

In the file manager, select the files to be added.

### Resource Classes

▪ **QMainwindow** ,
 
▪ **QDialog** , 

▪ **QLayout** , 

▪ **QLabel** , 

▪ **QPixmap** ,

▪ **QSqlDatabase** ,
   
▪ **QSqlQuery** ,

▪ **QMessageBox** , 

▪ **QCoreApplication** , 

▪ **QtDebug** , 

▪ **QSqlDriver** ,

▪ **QSpacerItem** ,

▪ **QtSql**.

## Part One:

 ▪ School management Application is in the MainWindow class, which inherits QMainWindow. QMainWindow provides the framework for windows that have menus, toolbars and dock windows.
 
 ▪ The application provides File, View and Help entries in the menu bar, with the following Actions:
 ![image](https://user-images.githubusercontent.com/75392302/152679480-b217df80-df63-465f-a2cb-1a8203440dfb.png)
![image](https://user-images.githubusercontent.com/75392302/152679501-ad6fc0e8-9d89-4567-a4e2-30d5527be88d.png
![image](https://user-images.githubusercontent.com/75392302/152679516-842dbec1-6c8c-4902-bb81-23ba9a2a4005.png)

### Login window

This dialog prompts the user to select in which mode he will login ( student, taecher or administrator ). 
 
 First we Create a Form Class,
 
 Using the designer obtain the following  form:![image](https://user-images.githubusercontent.com/75392302/152680101-d2344e76-1477-426e-98bd-11763f39e3e0.png)

And we add a private Slots to direct user to Login Form
```cpp
private slots:
    void on_student_clicked();

    void on_teacher_clicked();

    void on_admin_clicked();

    void showAbout();
```
**Admin Login**

Clicking on Admin Login show a dialog. This dialog prompts the user to enter the username and password to go to the main window of the applicaton.
This dialog prompts the user to enter the username and password to go to the main window of the applicaton.

 For this Version You can use `AnassBelcaid` as a username an `CPP` as password.![image](https://user-images.githubusercontent.com/75392302/152680517-edaf2eaa-9e06-47fe-a8f4-64a33f7ac07b.png)

so we go to the Login Database and we verify if the it contains the entered values , if yes we show mainwindow if not we show a warning  message;

Admin Tasks:
![image](https://user-images.githubusercontent.com/75392302/152680637-67ca2ff6-ef92-4ad4-ad07-c7e48799712b.png)

***Add New Student***

![image](https://user-images.githubusercontent.com/75392302/152680851-b741f528-f35b-4066-b7ac-0c15195da8c1.png)

When the admin add a student we automaticaly add a new user in student login database:

```cpp
db = QSqlDatabase::addDatabase("QSQLITE");
    db.setDatabaseName("C:\\Users\\Hello\\Desktop\\ProjectDatabase\\studentlogin.db");
    if(!db.open())
        QMessageBox::critical(this,"Error","could not open the database");

    //Add user
    auto query = new QSqlQuery(gtdb);
    QString user{"insert into LoginStudent values('"+fname+lname+"','"+Studentreg+"' )"};
    if(!query->exec(user))
        QMessageBox::critical(this,"Error","could not add the user");

    db.close();
```
***Search/Delete/Edit Student Details***
![image](https://user-images.githubusercontent.com/75392302/152682459-0359018f-5fea-4b3d-aeb1-63c3ca3fc043.png)
![image](https://user-images.githubusercontent.com/75392302/152682496-2b6b9cf5-ea0c-4cec-b520-17078d8ca73e.png)
![image](https://user-images.githubusercontent.com/75392302/152682586-846d7d27-9cc2-4085-a203-96660085cb98.png)
 
 So I can search of a student' details if only I know his register number.
 
 I can update Register number ,name , date of birth and Program name .
 
 As I can delete a student from system.
 
 ***View/Update student' Notes:
 ![image](https://user-images.githubusercontent.com/75392302/152682964-6d5dc7f8-2f0b-4d9c-b0d9-9637462d78ae.png)
![image](https://user-images.githubusercontent.com/75392302/152682997-6ee9ae91-4b43-48b3-b9e4-9271700f5f1f.png)
![image](https://user-images.githubusercontent.com/75392302/152683078-6a754091-cd13-4cf9-a170-97602f9add42.png)




```cpp
 


 
 
