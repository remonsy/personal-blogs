# personal-blogs
workspace
The Requirements Specification source file is in banch Software-Requirements-Specification
  
Software Requirements  Specification  
  
Personal Blog System  
      
May 5, 2017  
  
    
  
 
    
  
 
  
  
 
 
 
 
 
 
  
  	  
 
Table of Contents 
1. Introduction	1 
1.1 Purpose	1 
1.2 Scope	1 
1.3 Definitions, acronyms, and abbreviations	1 
1.4 References	2 
2. Overall description	2 
2.1 Product perspective	2 
2.3 User characteristics	4 
2.4 Constraints	4 
2.5 Assumptions and dependencies	4 
2.6 Apportioning of requirements	4 
3. Specific requirements	4 
3.1.1 User interfaces	5 
3.1.2 Hardware interfaces	5 
3.2 Functional requirements	5 

   
i    
 
 
1. Introduction  
  
Blog is a carrier with the network. It’s quick and easy to publish their own experience and communicate with others. It set a variety of personalized display and an integrated platform. This section gives a scope description and overview of everything included in this SRS document. Also, the purpose for this document is described and a list of abbreviations and definitions is provided.      
1.1 Purpose  
The preparation of this requirement has laid the foundation for the realization of the personal blog system, defined the detailed requirements of the personal blog system, and it is also the basis for project planning, summary design and detailed design. The purpose of this document is to give a detailed description of the requirements for the “Personal Blog System”. It will illustrate the purpose and complete declaration for the development of system. The expected readership is the decision maker, developer who is associated with the development of the personal blog system software. This product is designed for the needs of blog users, you can complete the blog user registration, login, publish, browse, modify blog, upload, browse photos, messages and other major functions. 
1.2 Scope  
The “Personal Blog System” is designed for the needs of blog users, you can complete the blog user registration, login, publish, browse, modify blog, upload, browse photos, messages and other major functions. It is a carrier with the network. Personal blog is to enable blog users to publish and comment on related blogs on the web. Use the Chinese programming language to complete its function independently.   
Bloggers can publish, edit, delete articles, as well as blog classification, archiving, personal information maintenance and other functions. Administrators can manage the user, and recommend the blog automatically to achieve sensitive information filtering. Visitors can read and comment on articles, bloggers on the blog, pay attention to bloggers, bloggers on the point of praise. 
The system can provide users with faster response speed. The system has no obvious security vulnerabilities, reports SQL injection and XSS cross-site scripting. 
1.3 Definitions, acronyms, and abbreviations  
	 Table  1 - Definitions 	 
Term  	Definition  
Visitor 	Someone who interacts with the mobile phone application  
Blogger  	System administrator who is given specific permission for managing and controlling the system  
Administrator  	Someone who has a restaurant and wants his restaurant to be a part the application  
Web-Portal  	A web application which present special facilities for blogger and administrator 
SQL 	Structured Query Language 
  
  
1.4 References   
[1]	IEEE Software Engineering Standards Committee, “IEEE Std 830-1998, IEEE Recommended Practice for Software Requirements Specifications”, October 20, 1998.  
[2]	Feldt R,”re_lecture5b_100914”, unpublished.  
  
[3]	Davis M A, “Just Enough Requirements Management: Where Software Development Meets Marketing”, New York, Dorset House Publishing, 2005.   
  
[4]	Karlsson J, “A Cost-Value Approach for Prioritizing Requirements”, Norges 
TekniskNaturvitenskapelige Uni. 1997  
  
1.5 Overview  
The remainder of this document includes three chapters and appendixes. The second one provides an overview of the system functionality and system interaction with other systems. This chapter also introduces different types of stakeholders and their interaction with the system. Further, the chapter also mentions the system constraints and assumptions about the product.  
The third chapter provides the requirements specification in detailed terms and a description of the different system interfaces. Different specification techniques are used in order to specify the requirements more precisely for different audiences.  
The fourth chapter deals with the prioritization of the requirements. It includes a motivation for the chosen prioritization methods and discusses why other alternatives were not chosen.   
The Appendixes in the end of the document include the all results of the requirement prioritization and a release plan based on them.  
  
  	  
2. Overall description  
This section will give an overview of the whole system. The system will be explained in its context to show how the system interacts with other systems and introduce the basic functionality of it. It will also describe what type of stakeholders that will use the system and what functionality is available for each type. At last, the constraints and assumptions for the system will be presented.  
2.1 Product perspective  
The system will consist of two parts : an application and a web portal. The application will be used to find the blogger and blog about the information and implementation of release, the portal will manage the access and edit demand management. 
 
The application needs to communicate with the user or administrator, and then interact with the program, has found the location of the user. Due to this product oriente a data, text, it need somewhere to store the data. Therefore, will use a database. However, applications and portals will communicate with the database in different ways. The application only uses the database to get the data, and the portal will also add and modify the data.  
The application has some restrictions about the resource allocation. To avoid problems with overloading the operating system the application, to provide a faster response speed for user, It should reduce unnecessary HTTP requests; use CND to publish content; use a long Expirse. It can make these components are cached and next time you visit, you can reduce unnecessary HTPP requests, so as to improve the speed of loading. 
2.2 System functions  
Blog is take the network as the carrier, which release their own experience and communicate with others and show own personality. 
Web log: Personal expression  2.Personal collection, Organize your own articles in chronological order according to the contents of the list  3.Personality display：Show your style  4.Bo:make a lot of Cherish the same ideals and follow the same path friend   6.Improve personal influence 
Visitor: Read Blog 
            Comment Blog 
	   	     Leave messages to blogger 
	   	     Pay attention to Blog 
Send private letter 
	  	     Mark like and give a reward 
Blogger: Post, edit, delete &read blog 
            Classified, file the blog 
   Management for comment of blog 
   Message management 
   Personal info maintain 
   To pay attention to other bloggers 
Admin: User Management 
      Blog management and can recommend blog 
  Auto Automatic filtering sensitive information 
 
The portal will provide management system and personal portal information management capabilities, and provide system updates tips.  
2.3 User characteristics  
There are three types of user interaction with the system: visitors, bloggers, administrators. These three types of users have different use of the system, so everyone has their own requirements. 
 
Visitors can use the application to read blogs, comments, attention to bloggers, send private messages, praise and reward. This means that visitors can search for blogs according to their own needs. In order for the users to get a relevant search result there are multiple criteria the users can specify and all results matches all of those.  
 
Bloggers use the portal site. They will manage their blog information, such as blog post, edit, delete, Bowen classification, personal information maintenance. 
 
Administrators also use portal sites. They manage the entire system, so there is no incorrect information. The administrator can sort out each user information and Bo Wen information.   
2.4 Constraints  
The Internet connection is also a constraint for the application. Since the application fetches data from the database over the Internet, it is crucial that there is an Internet connection for the application to function.  
Because of communication with a database, so the database information is a key constraint in the database. Due to sharing at both ends of the application, so it may be forced to incoming requests are queued, thus increasing the data for the time. 
  
2.5 Assumptions and dependencies  
A hypothesis about the product is that it is on the mobile application side, because the phone does not have enough hardware resources, resulting in the program can’t work. 
 
Another assumption about the product is that it is not possible to log on at the same time as two pages. 
   
2.6 Apportioning of requirements  
In the case that the project is delayed, there are some requirements that could be transferred to the next version of the application. Those requirements are to be developed in the third release, see Appendix IV.  
 
3. Specific requirements  
A good server that can connect to the network , remote FTP transmission and provide services.  
3.1 External interface Requirements  
Require a PC compatible with an i3 microprocessor or higher, with more than 1 gb of memory.The system uses a 120gb hard disk space server operating system for Windows 7 or Windows 8 10.  
3.1.1 User interfaces  
User interface: this system USES the graphical user interface, the mouse and the keyboard are the user interface, convenient user to the blog system's effective operation.Better communicate in your blog. Blog registration management module is used to establish the blog website fixed customer base, by recording the corresponding blog archives, realize the background of blog information maintenance and management, the latest development of archives will also facilitate the blog site and related enterprise information easily conveyed to every potential customers. 
 
 
Blogs and articles retrieval query module for network users with convenient search, and log read browse function, at the same time of log information, blog recommendation will also be able to timely feedback to network users. 
The blog personal maintenance management module is used to implement the user's dynamic management of blog profiles and related information.  
 
3.1.2 Hardware interfaces  
Require a PC compatible with an i3 microprocessor or higher, with more than 1 gb of memory.The system uses a 120gb hard disk space server operating system for Windows 7 or Windows 8 10. The browser is IE6.0 and above.Intel486 series, AMD K6 series and other PC desktops and portable computers;Runtime footprint: less than 1MB;Required hard disk space: less than 5MB  
 .  
3.2 Functional requirements  
The majority of bloggers' login features include reading blogs, Posting comments, logging in and Posting messages. 
Reading blogs provide users with easy access to online reading of their interest. 
Comments are available for readers to post their own opinions on the blogs they read. 
Registered blog this system the real blog users, in order to meet user login the system to meet the demand of myself more, including published messages, etc. Personal blog management functions: published articles, article management, news management, personal information management. 
The blog login system can publish its own articles and make the most basic management of the articles published, including the revision and revision. 
Message management function: users check, comment and delete the information they receive. 
Personal details are made by blog users to their personal data, including the revision and revision. 
Functions of system management: user management, blog classification, announcement management, comment management, system maintenance. 
Blog categorization: the ability to make a type of blog entry for blog users. 
Review management: to enter the visitors to view the comments of this system management, and delete operations for has expired or bad comments, make blog update can be done in a timely manner, to facilitate the maintenance of website. 
The system maintenance function realizes the security of the system  
