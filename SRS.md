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
Student Service Database Registry</br>
Prepared by Juan Mata</br>
</p>





#   1. Introduction
##    1.1 Purpose
This document is meant to portray the features of the Students Social Service Database Registry or **SSSDR** (final name pending). It will explain the point and attributes of the system, such as the interfaces of the system, what the system will do, the constraints under which it must operate.
This document is intended for both the faculty service administrators that oversee the social work program and the developers of the system.

     
##    1.2 Scope
This software system will be a local server system for a local school faculty administrator. This system will be designed to maximize the administrator’s productivity by providing tools to assist in automating the database registry review, which would otherwise have to be performed manually. By maximizing the administrator’s work efficiency and production, the system will meet the administrator’s needs while remaining easy to understand and use. The software will facilitate communication between faculty administrators and students via E-Mail. Preformatted reply forms are used in every stage of the database registry progress through the system to provide a uniform review process; the location of these forms is configurable via the application’s maintenance options. The system also contains a relational database containing a list of timesheets,faculty administrators, and students.

In short words,the **SSSDR** will permit users to manage timesheets and leave time and generate, print or export corresponding reports related to that data. 
    

##    1.3 Definitions, acronyms, and abbreviations
Terms | Definition | 
--- | --- | 
*SSSRD* | `Students Social Service Database Registry` | 
*Faculty Administrators* |  `The people that are in charge of the Social Service program.` | 
*Students* | `Students that are conducting their social work.` | 
*Timesheets* |  ` Records ins and outs of the students.` |
*Database* |  `Collection of all the information monitored by this system.` |
*Registry* | `Place where registers or records are kept.` | 
*IEEE* | `Institute of Electrical and Electronic Engineers` | 
*PL* | `Programming Language` |
*F-#* | `Functions` |
*C-#* | `Constraints` |
*OS* | `Operating System` |
*A-#* | `Assumptions` |
*D-#* | `Dependencies` |
*CI-#* | `Communications Interfaces` |
*FR-#* | `Functional requirement` |
*NR-#* | `Non Functional Requirements` |
*Query* | `A question` |







            
##    1.4 References 
IEEE. IEEE Std 830-1998 IEEE Recommended Practice for Software Requirements Specifications. IEEE Computer Society, 1998.

##    1.5 Overview
The remainder of this document includes three chapters and appendixes.It describes the informal  and formal requirements and is used to establish a context for the technical requirements specification.
These sections are cross-referenced by topic; to increase understanding by both groups involved.

#   2.Overall Description
This software system is a new attempt to meet new automatize registry of students by making a system where faculty administrators can digitally view, create, modify, and share with other faculty a linear series of the student’s social work records. Students can view and self-evaluate their progress, but not modify and will be rewarded with a certificate that mark progress and achievements of their community hours.

##   2.1 Product Perspective
1. The software system will be independent and self-contained.
2. The software system will be coded in PL C#.
3. The software system will have a SQL Database.
4. The software system will have external entities(such as a barcode scanner).
5. The software system interface will be easy to follow.

##   2.2 Product Functions
Function	   | Description|
--- | --- |
F-1	   |Faculty administrator registering.|
F-2	   |Student registering.|
F-3	   |Faculty administrator log-in.|
F-4	   |Student log-in.|
F-5	   |Software system connects a student account to a database.|
F-6	   |Software system creates a line of an overview so a student can access them and view their progress.|
F-7	   |Software system adds a timesheet to a report.|
F-8	   |Software system customize the interface of the report that shows the activities using a background and other modifiable graphics.|
F-9	   |Faculty administrator can view progress of a student.|
F-10	   |Faculty administrator access reports and associated timesheets.|
F-11	   |Faculty administrators can share reports with another faculty members.|
F-12	   |Faculty administrator validates work that student has done before the student is given points.|
F-13	   |Faculty administrator can modify database by add/drop/delete a registry of student.|
F-14	   |Software system can browse shared database.|
F-15	   |Software system can create a copy of a shared database which is then modifiable by the Faculty administrator.|
F-16	   |Faculty administrator can make a copy of a database they own.|
F-17	   |System Admins can temporarily change their account privileges to that of a Faculty administrator.|
F-18	   |System Admins can temporarily change their account privileges to that of a Student.|

##   2.3 User Characteristics
Actors	   | Description|
--- | --- |
Faculty Administrator	   | The Faculty Administrator is the person or people who are using the system to validate student registration, setting up activity reports for a student to access, link activities to outcomes or objectives, add timesheets to support the activities, manage how many points each activity is worth, viewing the progress of students, and a way to change the interface to make it more appealing through the use of custom software.|
System Administrator	   | The System Administrator can imitate any type of user in the system, can access and modify the database, and has all the privileges of all other user types.|
Student	   | The Student is the person or people who are using the system to register for an account, access activities, view timesheets linked to an activity, viewing their progress for each activity and overall points.|

##   2.4 Constraints
 Constraint	   | Description|
--- | --- |
 C-1	   | Must use student ID as a unique identifier for a student account.|
 C-2	   | All data shall be stored on SQL Engine.|
 C-3	   | All stored data shall be transferable in case of any manual reset.|
 C-4	   | Software system shall not be restricted by any OS.|
 C-5	   | Timesheet report shall be in a template showing school logo and administration when exported to a report.|
 C-6	   | Software system shall send a weekly reoprt via E-mail to a faculty administrator.|

##   2.5 Assumptions and Dependencies
 Assumption	   | Description|
 --- | --- |
 A-1	   | Assumed that the software system has no database limit.|
 A-2	   | Assumed that there is no mistake in student registry.|
 A-3	   | Assumed that there is no mistake in data compile when the software system is doing the report.|
 A-4	   | Assumed that all database shall be transferable.|
 
Dependencies	   | Description|
 --- | --- |
 D-1	   | Depend that all database shall be transferable.|
 D-2	   | Depend that the software system shall send an E-mail report weekly.|
 D-3	   | Depend that all data shall be inserted correctly.|
 
#   3.Specific requirements
This section contains all of the functional and quality requirements of the system. It gives a detailed
description of the system and all its features. 
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

1. A first-time user of the system should see the log-in page when he/she opens the application. See Figure 2, If the user has not registered, he/she should be able to do that on the log-in page.

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
Since the software system application does not have any designated hardware, it does not have any direct hardware interfaces. The physical system is managed by the application and the hardware connection to the database server is managed by the underlying operating system.

## 3.3 Software interfaces
The application communicates with the software system in order to get database information. The communication between the database and the application consists of operation concerning both reading and modifying the data, while the communication between the database and the application consists of only reading operations.

## 3.4 Communications interfaces
The communication between the different parts of the system is important since they depend on each
other.

Communications Interfaces	   | Description|
 --- | --- |
 CI-1	   | The system shall send a notification to the user to inform them of time approval or rejection.|
 CI-2	   | The system shall send an email message to confirm registration with the system.|
 CI-3	   | The system shall send a notification to inform the user of new email messages, instant messages, or calendar event invitations.|
## 3.5 Functional Requirements
Functional Requirements   | <br>| Description|
--- | --- |--- |
FR-1	   | Student Add |The system shall let a User that is an administrator with correct permissions who is logged into the system to add students.|
FR-2	   | Student  Change/Cancel |The system shall let a user that is an administrator with correct permissions who is logged into the system to abandon the process of changing an students (add/delete/edit) without submitting changes.|
FR-3	   | Student Edit |The system shall let a user that is an administrator with correct permissions who is logged into the system to edit students.|
FR-4	   | Student Remove |The system shall let a user that is an administrator with correct permissions who is logged into the system to remove students.|
FR-5	   | Student Review |The system shall let a user that is an administrator with correct permissions who is logged into the system to review students.|

### 3.5.1 Description of functional requirements by giving various Use Case.
>Use Case related to **Installation**.

`Use Case 1`	   |  <br>|  <br>|  
 --- | --- | --- | 
  <br>|`Primary Actor`	   | User|
  <br>|`Pre-condition`	   | Have .zip file of the software at hand and do installation of programs in order.|
  <br>|`Main Scenario`	   | Installation|
  <br>| **Setp 1** | Install **SQL Server 2016 LocalDB**, which is located on the installation **SetupChecador.zip** file, named as: `SqlLocalDB.msi` |
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
   <br>| **Setp 1** |  Install **Chocador Asistencia.app**, which is located on the installation **SetupChecador.zip** file, named as: `Setup Checador.msi`|
   <br>| **Setp 2** |  Before starting installation, `read all the contents of the installation window`. |
   <br>| **Setp 3** |  Having read all the content, click **Siguiente**. |
   <br>| **Setp 4** |  Select folder location, where **Chocador Asistencia.app** installation will take place. |
   <br>| **Setp 5** |  Choose if the installation of **Chocador Asistencia.app** will be in all users or in a single user of the system. |
   <br>| **Setp 6** |  When finished click on **Siguiente**. |
   <br>| **Setp 7** |  Confirm Installation. |
   <br>| **Setp 8** |  The installer is ready to install **Chocador Asistencia.app** on the computer. |
   <br>| **Setp 9** |  Click **Siguiente** to begin the installation. |
   <br>| **Setp 10** |  Installation complete. |
   <br>| **Setp 11** |  **Chocador Asistencia.app** installed correctly |
   <br>| **Setp 12** |  Click on **Cerrar** to exit the window. |
   <br>| **Setp 13** |  Use **Windows Update** to verify any important updates to the .NET Framework. |
   <br>| **Setp 14** |  Ready, installation completed. |
   <br>| **Setp 15** |  **Chocador Asistencia.app** will appear on the desktop of the device. |
   <br>| **Setp 16** |  Click on **Chocador Asistencia.app** to start use. |
   
>Use Case related to **Registry**.

`Use Case 2`	   |  <br>|  <br>|  
 --- | --- | --- | 
  <br>|`Primary Actor`	   | User|
  <br>|`Pre-condition`	   | Correct installation of **Chocador Asistencia.app**.|
  <br>|`Main Scenario`	   | Registry of students|
  
 >Use Case related to **Consult**.

`Use Case 3`	   |  <br>|  <br>|  
 --- | --- | --- | 
  <br>|`Primary Actor`	   | User|
  <br>|`Pre-condition`	   | Correct registry of students.|
  <br>|`Main Scenario`	   | Consult of registry of students|
  
>Use Case related to **Export**.

`Use Case 4`	   |  <br>|  <br>|  
 --- | --- | --- | 
  <br>|`Primary Actor`	   | User|
  <br>|`Pre-condition`	   | Correct consult of registry of students.|
  <br>|`Main Scenario`	   | Export of registry of students|
  
>Use Case related to **Export Excel File**.

`Use Case 5`	   |  <br>|  <br>|  
 --- | --- | --- | 
  <br>|`Primary Actor`	   | User|
  <br>|`Pre-condition`	   | Correct export of registry of students|
  <br>|`Main Scenario`	   | Export Excel File|
  
>Use Case related to **Modification**.

`Use Case 6`	   |  <br>|  <br>|  
 --- | --- | --- | 
  <br>|`Primary Actor`	   | User|
  <br>|`Pre-condition`	   | Correct registry of student **ID**.|
  <br>|`Main Scenario`	   | Modification of registry of students|
  
>Use Case related to **Uninstall**.

`Use Case 7`	   |  <br>|  <br>|  
 --- | --- | --- | 
  <br>|`Primary Actor`	   | User|
  <br>|`Pre-condition`	   | None.|
  <br>|`Main Scenario`	   | Uninstalling **Chocador Asistencia.app**|
  
## 3.6 Nonfunctional Requirements
Nonfunctional Requirements	   | Description|
 --- | --- |
NR-1	   | Responses to queries shall take no longer than 5 seconds to load onto the screen after the user submits the query.|
NR-2	   | All documentation generated by the system shall be fully downloadable.|

#   4.Supporting Information
