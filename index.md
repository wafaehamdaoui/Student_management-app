## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/wafaehamdaoui/Student_management-app/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.


### Markdown
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
 

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/wafaehamdaoui/Student_management-app/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
