# __**A walkthrough of creating and dropping databases and tables.**__

 __**The journey began by accessing the AWS EC2 environment. 
 This step sets the foundation for all subsequent database operations.**__

  - Access AWS Console
  - Navigate to EC2 Dashboard

<img width="609" height="673" alt="image" src="https://github.com/user-attachments/assets/ebb44f75-4189-48c4-af80-da327b88a973" />

___

__**After launching the EC2 instance, I accessed the terminal and navigated 
to the working directory to prepare for database interaction.**__ 

<img width="601" height="668" alt="image" src="https://github.com/user-attachments/assets/20db6456-a2a3-465c-a6d9-22200017c267" />

___

__**Using MariaDB, I connected with root credentials and created a 
new database named world. The SHOW DATABASES command confirmed its successful creation.**__

<img width="605" height="671" alt="image" src="https://github.com/user-attachments/assets/35f9634a-661c-4d7f-8d64-3d11c1e05c36" />

___

__**I defined the country table with multiple fields including code, name, continent, and 
more. The SHOW TABLES command confirmed its presence.**__

<img width="603" height="654" alt="image" src="https://github.com/user-attachments/assets/aa546c16-8960-438b-8522-d1952996b33f" />

___

__**The SHOW COLUMNS command revealed the schema of the country table, including data 
types, nullability, and default values.**__

<img width="602" height="659" alt="image" src="https://github.com/user-attachments/assets/34a6a9e5-cc52-4bd3-821a-c785a2aae6b2" />

___

__**I created a secondary table city, inspected its structure, and then dropped it using 
DROP TABLE. The final command confirmed its deletion.**__

<img width="603" height="671" alt="image" src="https://github.com/user-attachments/assets/4e7ad7ab-29ce-4963-b079-fcdf0736f4db" />

<img width="600" height="668" alt="image" src="https://github.com/user-attachments/assets/ad71deff-cb64-4a56-836b-35059b58c090" />

___


__**I learned how data is organized into tables with rows and columns, how relationships 
are defined between them, and how SQL is used to interact with that data. I practiced 
using SQL commands, which helped me understand how to define schemas, enforce data 
integrity, and evolve the database structure over time, in addition to exploring 
how to assign appropriate data types to ensure validity for queries.**__

