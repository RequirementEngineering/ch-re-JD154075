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
This SRS document is to present a detailed description of the Students Social Service Database Registry or **SSSDR** (final name pending). It will explain the point and attributes of the system, such as the interfaces of the system, what the system will do, the constraints under which it must operate.
This document is intended for both the faculty service administrators that oversee the social work program and the developers of the system.

     
##    1.2 Scope
This software system will be a local server system for a local school faculty administrator. This system will be designed to maximize the administrator’s productivity by providing tools to assist in automating the database registry review, which would otherwise have to be performed manually. By maximizing the administrator’s work efficiency and production, the system will meet the administrator’s needs while remaining easy to understand and use. The software will facilitate communication between faculty administrators and students via E-Mail. Preformatted reply forms are used in every stage of the database registry progress through the system to provide a uniform review process; the location of these forms is configurable via the application’s maintenance options. The system also contains a relational database containing a list of timesheets,faculty administrators, and students.

In short words,the **SSSDR** will permit users to manage timesheets and leave time and generate, print or export corresponding reports related to that data. 
    

##    1.3 Definitions, acronyms, and abbreviations
Terms | Definition | 
--- | --- | 
*SSSRD* | `Students Social Service Database Registry` | 
*Faculty Administrators* |  `The people that are in charge of the Social Service program.` | 
*Students* | `Stuents that are conducting their social work.` | 
*Timesheets* |  ` Records ins and outs of the students.` |
*Database* |  `Collection of all the information monitored by this system.` |
*Registry* | `Place where registers or records are kept.` | 
*IEEE* | `Institute of Electrical and Electronic Engineers` | 
*PL* | `Programming Language` |
*F* | `Functions` |

            
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
F-8	   |Software system customizes the interface of the report that shows the activities using a background and other modifiable graphics.|
F-9	   |Faculty administrator can view progress of a student.|
F-10	   |Faculty administrator accesses reports and associated timesheets.|
F-11	   |Faculty administrators can share reports with another faculty members.|
F-12	   |Faculty administrator validates work that student has done before the student is given points.|
F-13	   |Faculty administrator can modify database by add/drop/delete a registry of student.|
F-14	   |Software system can browse shared database.|
F-15	   |Software system can create a copy of a shared database which is then modifiable by the Faculty administrator.|
F-16	   |Faculty administrator can make a copy of a database they own.|
F-17	   |System Admins can temporarily change their account privileges to that of a Faculty administrator.|
F-18	   |System Admins can temporarily change their account privileges to that of a Student.|

##   2.3 User Characteristics
##   2.4 User Characteristics
##   2.5 Assumptions and Dependencies

#   3.Specific requirements


#   4.Supporting Information
