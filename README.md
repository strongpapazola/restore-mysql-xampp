# restore-mysql-xampp

STOP! Please do NOT delete ibdata1 file!

Deleting this file is like playing a Russian roulette with your databases, it could work and restablish everything, but also, probably could leave unusable every database you have.

Instead, first try using the MySQL backup folder which is included with XAMPP. So do the next:

Rename the folder mysql/data to mysql/data_old (you can use any name)
Create a new folder mysql/data
Copy the content that resides in mysql/backup to the new mysql/data folder
Copy all your database folders that are in mysql/data_old to mysql/data (skipping the mysql, performance_schema, and phpmyadmin folders from data_old)
Finally copy the ibdata1 file from mysql/data_old and replace it inside mysql/data folder
Start MySQL from XAMPP control panel
And, voilà!
