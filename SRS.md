<p align="center">
Universidad Autonoma de Ciudad Juarez</br>
División Multidisciplinaria de Ciudad Universitaria</br>
Departamento de Ingeniería Electricidad y Computación</br>
</p>
<br>
<p align="center">
<img width="270" height="270" 
  src="http://www.uacj.mx/comunicacion/PublishingImages/Escudo%20UACJ%202015/Escudo%20uacj%202015-color-sin%20fondo.png">
</p>
<br>
<p align="center">
Software Requirements Specification</br>
for</br>
Laboratorial Timesheets Database Registry</br>
Prepared by Juan Mata</br>
</p>





#   1. Introduction
##    1.1 Purpose
This document is meant to portray the laboratory's automatized timesheet database registry project named as **Chocador Asistencia**. By explaining it's purpose; such as it's overall description, it's dos and don'ts,it's interface and it's actions after it's development. 
This document is intended for both the **Laboratory Director** that oversee the work program and the **Developers** of the software program.

##    1.2 Scope
This software program will be a **local server** system for a **standalone machine** for the school's laboratory director. 
This software program will be designed to maximize the laboratory director’s productivity by providing tools to assist in automating the timesheet database registry, which would otherwise have to be performed manually. By maximizing the laboratory director’s work efficiency and production, the software program will meet the laboratory director’s needs while remaining easy to understand and use. The software program will facilitate communication between the laboratory director,other faculty and students. A preformatted form is used in every stage of the timesheet database registry progress through the system to provide a uniform review process; the location of these form is configurable via the program’s maintenance options.

In short words,**Chocador Asistencia** will permit the school's laboratory director to manage automated timesheets,where he can export corresponding reports related to that data.

##    1.3 Definitions, acronyms, and abbreviations
Terms | Definition | 
--- | --- | 
*Laboratory director* |  `The person that is in charge of the laboratory's management and it's programs.` | 
*Service Administrators* |  `Users that have unrestricted access to service configuration, can perform all service administrative tasks and all operations in Managed Domains.` | 
*Faculty* |  `The body of teachers and administrators at a school.` | 
*Students* | `Students that are conducting their social work.` |
*Developers* | `The people that develop the software program.` |
*Local Server* |  `Server that is running in a local or a mounted folder and whose document root is NOT the parent of the project root.` |
*Standalone Machine* | `Device is any mechanism or system that can perform its function without the need of another device, computer, or connection.` |
*Timesheets* |  `Detailed records showing the amount of time spent on each program or student.` |
*Database* |  `Collection of all the information monitored by this system.` |
*Registry* | `Place where registers or records are kept.` | 
*IEEE* | `Institute of Electrical and Electronic Engineers` | 
*Programming Language* | `A vocabulary and set of grammatical rules for instructing a computer or computing device to perform specific tasks.` |
*C#* | `Pronounced C sharp, is a general-purpose, multi-paradigm programming language encompassing strong typing, lexically scoped, imperative, declarative, functional, generic, object-oriented (class-based), and component-oriented programming disciplines.` |
*F-#* | `Functions` |
*C-#* | `Constraints` |
*A-#* | `Assumptions` |
*D-#* | `Dependencies` |
*CI-#* | `Communications Interfaces` |
*FR-#* | `Functional requirement` |
*NR-#* | `Non Functional Requirements` |
*Q&A* | `Questions and Answers` |
            
##    1.4 References 
IEEE. IEEE Std 830-1998 IEEE Recommended Practice for Software Requirements Specifications. IEEE Computer Society, 1998.

##    1.5 Overview
The remainder of this document describes the formal requirements and is used to establish a context for the technical requirements specification.
*These sections are cross-referenced by topic; to increase understanding by both groups involved.*

#   2.Overall Description
This software program is a new attempt to meet new automatize registry of timesheets by making a system where the laboratory director can digitally view, create, modify, and share with other faculty a linear series of the time records such as; 
>1.Student's time in work program or social work.*Students can view and self-evaluate their progress, but not modify.
<br> >Students will be rewarded with a certificate that mark their progress and achievements of their work hours*.<br>
>2.Faculty time usage of laboratorys and it's equipments.

##   2.1 Product Perspective
1. The software program will be independent and self-contained.
2. The software program will be coded in programming language C#.
3. The software program will have a SQL Database.
4. The software program will have external entities,*such as a barcode scanner*.
5. The software's program interface will be easy to follow.
6. The software program will have a backup database protocol to follow.
7 The software program will have a security protocol to follow when attempting to modify information in the database registry.

##   2.2 Product Functions
Function	   | Description|
--- | --- |
F-1	   |Laboratory director registering.|
F-2	   |Faculty registering.|
F-3	   |Student registering.|
F-4	   |Laboratory director log-in.|
F-5	   |Faculty log-in.|
F-6	   |Student log-in.|
F-7	   |The software program connects a faculty account to a database.|
F-8	   |The software program connects a student account to a database.|
F-9	   |The software program creates a line of an overview so a student or faculty can access them and view their progress.|
F-10	   |The software program adds a timesheet to a report.|
F-11	   |The software program customize the interface of the report that shows the activities using a background and other modifiable graphics.|
F-12	   |The laboratory director has administrative privileges of the software program.|
F-13	   |The laboratory director can view progress of a student.|
F-14	   |The laboratory director can access reports and associated timesheets.|
F-15	   |The laboratory director can share reports with another faculty members.|
F-16     |The laboratory director validates work that student has done before the student is given points.|
F-17	   |The laboratory director can modify the database registry of student by add/drop/delete.|
F-18	   |The software program can browse shared database.|
F-19	   |The software program can create a copy of a shared database which is then modifiable by the laboratory director.|
F-20	   |The developer of the software program can temporarily change their account privileges to that of a laboratory director.|
F-21	   |The developer of the software program can temporarily change their account privileges to that of a faculty or a student.|

##   2.3 User Characteristics
Actors	   | Description|
--- | --- |
Laboratory Director	   | The laboratory director is the person who is using the program to validate student and faculty registration, setting up activity reports, link activities to outcomes or objectives, add timesheets to support the activities, viewing the progress of students work, and activities of faculty usage of the laboratories and equipment.|
Developer	   | The developer can imitate any type of user in the system, can access and modify the database, and has all the privileges of all other user types, he or she is more like a system administrator.|
Faculty	   | The faculty is the person or people who are using the program to register for an account, access laboratories and equipment, view timesheets linked to an activity, viewing their progress for each activity and overall take.|
Student	   | The student is the person or people who are using the program to register for an account, access activities, view timesheets linked to an activity, viewing their progress for each activity and overall points.|
Service Administrator	   | The service administrator is the person or people,who have unrestricted access to service configuration, can perform all service administrative tasks and all operations in managed domain of the school's electrical department.|

##   2.4 Constraints
 Constraint	   | Description|
--- | --- |
 C-1	   | Must use a service administrator ID as a unique identifier for the installation of the software program.|
 C-2	   | Must use laboratory directo ID as a unique identifier for administrative privileges of the software program.|
 C-3	   | Must use faculty ID as a unique identifier for a faculty account.|
 C-4	   | Must use student ID as a unique identifier for a student account.|
 C-5	   | All data shall be stored on SQL Engine.|
 C-6	   | All stored data shall be transferable in case of any manual reset.|
 C-7	   | The software program shall not be restricted by any operating system.|
 C-8	   | The timesheet report shall be in a template showing school logo and administration when exported to a report.|
 C-9	   | The software program shall send a weekly reoprt via E-mail to the laboratory director.|
 C-10	   | The software program should always be running.|

##   2.5 Assumptions and Dependencies
 Assumption	   | Description|
 --- | --- |
 A-1	   | Assumed that the software program has no database limit.|
 A-2	   | Assumed that there is no mistake in faculty registry.|
 A-3	   | Assumed that there is no mistake in student registry.|
 A-4	   | Assumed that there is no mistake in data compile,when the software program is doing the report.|
 A-5	   | Assumed that all the database shall be transferable.|
 A-6	   | Assumed that the software program is running when making a login.|
 A-6	   | Assumed that the login section of the software's program registry, logs in correctly when using a barcode scanner.|
 
Dependencies	   | Description|
 --- | --- |
 D-1	   | Depend that all database shall be transferable.|
 D-2	   | Depend that the software program shall send an E-mail report weekly.|
 D-3	   | Depend that all data shall be inserted correctly.|
 D-4	   | Depend that the sotware program is running when making a login.|
 A-5	   | Depend that the login section of the software's program registry, logs in correctly when using a barcode scanner.|
 
 
#   3.Specific requirements
This section contains all of the functional and quality requirements of the program. It gives a detailed
description of it's features. 
## 3.1  User interfaces

<br>
<p align="center">
<img width="200" height="200" alt="Figure 1"
  src="https://github.com/RequirementEngineering/ch-re-JD154075/blob/master/SRS_Images/User%20interfaces_Images/1.png">
</p>
<p align="center">
Figure 1
</p>
<br>

1. A first-time user of the program should see the log-in page when he/she opens the application. If the user has not registered, he/she should be able to do that on the log-in page.See Figure 2.

<br>
<p align="center">
<img width="200" height="200" alt="Figure 1"
  src="https://github.com/RequirementEngineering/ch-re-JD154075/blob/master/SRS_Images/User%20interfaces_Images/2.png">
</p>
<p align="center">
Figure 2
</p>
<br>

2. If the user is not a first-time user, he/she should be able to see the search page directly when the
application is opened, see Figure 3. Here the user chooses the type of search he/she wants to conduct.

<br>
<p align="center">
<img width="200" height="200" alt="Figure 1"
  src="https://github.com/RequirementEngineering/ch-re-JD154075/blob/master/SRS_Images/User%20interfaces_Images/3.png">
</p>
<p align="center">
Figure 3
</p>
<br>

3. Every user should have a profile page where they can edit their name,ID,e-mail address, and phone number ,see Figure 4. 

<br>
<p align="center">
<img width="300" height="200" alt="Figure 1"
  src="https://github.com/RequirementEngineering/ch-re-JD154075/blob/master/SRS_Images/User%20interfaces_Images/4.png">
</p>
<p align="center">
Figure 4
</p>
<br>

## 3.2 Hardware interfaces
The only designated hardware for this software program would be a barcode scanner and a physical keyboard.The software program itself does not have any direct hardware interfaces. The physical program is managed by an application and the hardware connection to the database server is managed by the underlying operating system.

## 3.3 Software interfaces
The application communicates with the software program in order to get database information. The communication between the database and the software program consists of operation concerning both reading and modifying the data, while the communication between the database and the application consists of only reading operations.

## 3.4 Communications interfaces
The communication between the different parts of the program is important since they depend on each
other.

Communications Interfaces	   | Description|
 --- | --- |
 CI-1	   | The software program shall send a notification to the user to inform them of time approval or rejection.|
 CI-2	   | The software program shall send a notification to confirm registration with the database.|
 CI-3	   | The software program shall read correctly the barcode scanner,while writing.|
 
## 3.5 Functional Requirements
Functional Requirements   | <br>| Description|
--- | --- |--- |
FR-1	   | Faculty/Student Add |The software program shall let a User that is an administrator with correct permissions who is logged into the program to add faculty or students.|
FR-2	   | Faculty/Student  Change/Cancel |The software program shall let a user that is an administrator with correct permissions who is logged into the program to abandon the process of changing information of a faculty or student (add/delete/edit) without submitting changes.|
FR-3	   | Faculty/Student Edit |The program shall let a user that is an administrator with correct permissions who is logged into the program to edit faculty or student information.|
FR-4	   | Faculty/Student Remove |The program shall let a user that is an administrator with correct permissions who is logged into the program to remove  faculty or students.|
FR-5	   | Faculty/Student Review |The system shall let a user that is an administrator with correct permissions who is logged into the program to review faculty and students.|

## 3.6 Nonfunctional Requirements
Nonfunctional Requirements	   | Description|
 --- | --- |
NR-1	   | Responses to queries shall take no longer than 5 seconds to load onto the screen after the user submits the query.|
NR-2	   | All documentation generated by the system shall be fully downloadable.|


## 3.7 Description of *Functional Requirements* by giving various `Use Case`.
>Use Case related to **Installation**.

`Use Case 1`	   |  <br>|  <br>|  
 --- | --- | --- | 
  <br>|`Primary Actor`	   | Service Administrators/Laboratory Director|
  <br>|`Pre-condition`	   | Have administrative permission to download the software program, have the .zip file of the software program at hand and do installation of programs in the .zip file in order.|
  <br>|`Main Scenario`	   | Installation|
  <br>| **Note** |  `Need to have a service administrator's ID, for installation of the software program.` |
  <br>| **Setp 1** | Install **SQL Server 2016 LocalDB**, which is located on the installation file  **SetupChecador.zip**, named as: `SqlLocalDB.msi` |
   <br>| **Setp 2** |  Before starting installation, `read all the contents of the installation window`. |
   <br>| **Setp 3** |  Having read all the content, click **Siguiente**. |
   <br>| **Setp 4** |  Carefully read the following license agreement. |
   <br>| **Setp 5** |  Having read the contract and accepted the terms, click **Siguiente**. |
   <br>| **Setp 6** |  The configuration program is ready to **start** the **installation**. |
   <br>| **Setp 7** |  Click **Instalar** to begin the installation. |
   <br>| **Setp 8** |  It will take a few seconds to finish the installation of **Microsoft SQL Server 2016 LocalDB**. |
   <br>| **Setp 9** |  When installation is finished, read all the contents of the window that appears |
   <br>| **Setp 10** |  When finishing the revision of the window, we click on **Finalizar.**. |
   <br>| **Setp 11** |  Ready. |
   <br>| **Setp 12** |  In order for the configuration changes made in **Microsoft SQL Server LocalDB** to take **effect**, the system will have to **restart**. |
   <br>| **Setp 13** |  When accepting, click **Si**. |
   <br>| **Setp 14** |  After restarting the system, **Microsoft SQL Server 2016 LocalDB** will be installed. |
   <br>| <br> |  `Next step is to install the application.` |
   <br>| **Setp 1** |  Install **Chocador Asistencia** program, which is located on the installation file **SetupChecador.zip**, named as: `Setup Checador.msi`|
   <br>| **Setp 2** |  Before starting installation, `read all the contents of the installation window`. |
   <br>| **Setp 3** |  Having read all the content, click **Siguiente**. |
   <br>| **Setp 4** |  Select folder location, where **Chocador Asistencia** program installation will take place.*By default* `Documents/Checador Asistencia` |
   <br>| **Setp 5** |  Choose if the installation of **Chocador Asistencia** program will be in all users or in a single user of the system. |
   <br>| **Setp 6** |  When finished click on **Siguiente**. |
   <br>| **Setp 7** |  Confirm Installation. |
   <br>| **Setp 8** |  The installer is ready to install **Chocador Asistencia** program on the computer. |
   <br>| **Setp 9** |  Click **Siguiente** to begin the installation. |
   <br>| **Setp 10** |  Installation complete. |
   <br>| **Setp 11** |  **Chocador Asistencia.app** installed correctly |
   <br>| **Setp 12** |  Click on **Cerrar** to exit the window. |
   <br>| **Setp 13** |  Use **Windows Update** to verify any important updates to the .NET Framework. |
   <br>| **Setp 14** |  Ready, installation completed. |
   <br>| **Setp 15** |  **Chocador Asistencia.app** will appear on the desktop of the device. |
   <br>| **Setp 16** |  Click on **Chocador Asistencia** program to start use. |
   
>Use Case related to **Registry**.

`Use Case 2`	   |  <br>|  <br>|  
 --- | --- | --- | 
  <br>|`Primary Actor`	   | Laboratory Director/Faculty/Student|
  <br>|`Pre-condition`	   | Correct installation of **Chocador Asistencia** program.|
  <br>|`Main Scenario`	   | Registry of faculty and students|
  <br>| **Setp 1** | Click **Registrar** in the initial window. |
  <br>| **Setp 2** | Registration window will open. |
  <br>| **Setp 3** | Fill in requirements, correctly **Student ID restricted to  6 digits**. |
  <br>| **Setp 4** | After completing the query, click on **Registrar**. |
  <br>| **Setp 4** | If the registration was made correctly, it is saved and a window appears saying, `Se registro correctamente`> Click **OK** to continue. |
  
 >Use Case related to **Log in and log out**.

`Use Case 3`	   |  <br>|  <br>|  
 --- | --- | --- | 
  <br>|`Primary Actor`	   | Faculty/Student|
  <br>|`Pre-condition`	   | Correct registry of faculty or students.|
  <br>|`Main Scenario`	   | Log in and log out of faculty or students|
  <br>| **Setp 1** | Login. |
  <br>| **Setp 2** | Scan faculty or student ID or enter ID manually. |
  <br>| **Setp 3** | If faculty or student ID is scanned, it will be automatically registered and if it is entered manually, click on **Checar**. |
  <br>| **Setp 4** | If the faculty or student ID was entered correctly, a following window will appear showing `[ENTRADA]` together with the time of the last check in registry. |
  <br>| **Setp 5** | Log Out. |
  <br>| **Setp 6** | Scan faculty or student ID or enter ID manually. |
  <br>| **Setp 7** | If faculty or student ID is scanned, it will be automatically registered and if it is entered manually, click on **Checar**. |
  <br>| **Setp 8** | If the faculty or student ID was entered correctly, a following window will appear showing `[SALIDA]` together with the time of the last check in registry. |
  <br>| **Note** | If faculty or student ID is not registered or entered correctly a window will appear saying, `ERROR: MATRICULA NO ENCONTRADA`. |
  
 >Use Case related to **Consult**.

`Use Case 4`	   |  <br>|  <br>|  
 --- | --- | --- | 
  <br>|`Primary Actor`	   | Laboratory Director|
  <br>|`Pre-condition`	   | Correct registry of students and their registry of log in and log out.|
  <br>|`Main Scenario`	   | Consult of registry of faculty or students|
  <br>| **Setp 1** | To consult records click on **Consultar**  in the initial window. |
  <br>| **Setp 2** | Records query window will open. |
  <br>| <br> | `Search for records by Date.` |
  <br>| **Setp 3** | Select the **Fecha** box in the **Registros**  frame> Select the date range> Click on **Buscar**. *The record will appear on the right side.* |
  <br>| <br> | `Search of records by Student ID and Date.` |
  <br>| **Setp 4** | Select the **Fecha** and **Matrícula**  boxes in the **Registros** frame> Select the date range> Enter student ID> Click on **Buscar**.`The record will appear on the right side.` |
  <br>| <br> | `Search for Students by Student ID`|
  <br>| **Setp 5** | Select **Matrícula** in the **Estudiantes**  frame> Enter Student ID> Click on **Buscar** |
  <br>| <br> | `Search for Students by Name.` |
  <br>| **Setp 6** | Select **Nombre** in the **Estudiantes** frame> Enter Student name> Click on **Buscar** |
  <br>| <br> | `Total Search of Students in records.` |
  <br>| **Setp 7** | Select **Todos** in the **Estudiantes** frame> Click on **Buscar** |
  
  
>Use Case related to **Export**.

`Use Case 5`	   |  <br>|  <br>|  
 --- | --- | --- | 
  <br>|`Primary Actor`	   | Laboratory Director |
  <br>|`Pre-condition`	   | Correct consult of registrys of faculty or students.|
  <br>|`Main Scenario`	   | Export of registry of faculty or students|
  <br>| **Setp 1** | To export records click on **Exportar a Excel**. |
  <br>| **Setp 2** | It will take a few seconds to process. |
  <br>| **Setp 3** | A window asking for the save location of the exported record, will appear. |
  <br>| **Setp 4** | Fill in the requirements that is request. `File name is automatically filled in as` **Reporte** `and with the export date in dd / mm / yyyy format)> Click on Save.` |
  <br>| **Setp 5** | It will be saved in an Excel file. |
  <br>| **Setp 6** | If the record was saved correctly a window will appear saying `Archivo guardado correctamente`.> Click on **OK** to continue. |
  
 
>Use Case related to **Export Excel File**.

`Use Case 6`	   |  <br>|  <br>|  
 --- | --- | --- | 
  <br>|`Primary Actor`	   | Laboratory Director|
  <br>|`Pre-condition`	   | Correct exports of registrys of faculty or students|
  <br>|`Main Scenario`	   | Export Excel File|
  <br>| **Setp 1** | The export of the file in Excel appears in wherever location it is saved as such, with name `Reporte` and day of that is being exported. |
  <br>| **Setp 2** | The file exported in Excel is created with a default template for the school. |
  
>Use Case related to **Modification**.

`Use Case 7`	   |  <br>|  <br>|  
 --- | --- | --- | 
  <br>|`Primary Actor`	   | Laboratory Director|
  <br>|`Pre-condition`	   | Have laboratory's director unique ID, correct registry of faculty or student **ID**.|
  <br>|`Main Scenario`	   | Modification of registry of faculty or students|
  <br>| **Setp 1** | To be able to modify the registration of a student> Click on Modify. **Only Administrator can modify.** |
  <br>| **Setp 2** | A window will opened to modify the faculty or student registry. |
  <br>| **Setp 3** | To be able to **Modify** a record> Enter the student ID that you want to modify> Click on **Buscar**. |
  <br>| **Setp 4** | Registration of the faculty or student with that faculty or student ID will appear> Correct any incorrect aspect> To save any modification click on **Modificar**. |
  <br>| **Setp 5** | If the modification was made correctly, a window appears saying `Se modefico el estudiante correctamente`. |
  <br>| **Note** | If you want to **Delete** the registration of a certain faculty or student with certain faculty or student ID> Click on **Eliminar**. |
   
>Use Case related to **Database Backup**.

`Use Case 8`	   |  <br>|  <br>|  
 --- | --- | --- | 
  <br>|`Primary Actor`	   | Laboratory Director|
  <br>|`Pre-condition`	   | None.|
  <br>|`Main Scenario`	   | **Chocador Asistencia** program database backup|
  <br>| **Note** | In case you have to remove the program.**It is recommended to save the database** to continue using it, when the program is reinstalled.  |
  <br>| **Setp 1** | Access the folder where the program was installed *By default* `Documents/Checador Asistencia`.  |
  <br>| **Setp 2** | Inside `Documents/Checador Asistencia` > The two files **BaseDeDatos.mdf** and **BaseDeDatos_log.ldf** should be **copied** and **stored** in a **safe place**.  |
  <br>| **Setp 3** | When the program is installed again just paste these two files in the program folder by replacing the previous files by the same name.  |
  
>Use Case related to **Uninstall**.

`Use Case 9`	   |  <br>|  <br>|  
 --- | --- | --- | 
  <br>|`Primary Actor`	   | Laboratory Director/Service Administrators|
  <br>|`Pre-condition`	   | Database Backup.|
  <br>|`Main Scenario`	   | Uninstalling **Chocador Asistencia** program|
  <br>| **Setp 1** | Go to Control Panel> Programs> Uninstall Program> Search application: `Micosoft SQL Server 2016 LocalDB` and `Checador Asistencia `  |
  <br>| **Setp 2** | Select the programs one by one and click on **Uninstall**.  |
  
#   4.Supporting Information
## 4.1 Elicitation Process
>First Day Interview: Type: **Q&A**

Actors	   |  <br>|  <br>|  
 --- | --- | --- | 
  Developers|<br>	   | <br>|
  Laboratory Director|`Q&A`	   | <br>|
