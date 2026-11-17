# CLOUD-DATA-STORAGE-SERVER

### NAME: HAMDHAN
### REG NO: 212225020013

## Aim

To create and configure an Amazon Relational Database Service (Amazon RDS) instance as a cloud data storage server, configure the required security settings, connect it to a web application, and perform database operations using the application.

## Algorithm / Steps

1. Create a Security Group for the RDS database.
2. Add an inbound rule to allow MySQL (Port 3306) access from the Web Security Group.
3. Create a DB Subnet Group using two Availability Zones.
4. Launch an Amazon RDS MySQL database instance.
5. Configure the database with the required identifier, username, password, storage, and instance class.
6. Associate the database with the created Security Group and Subnet Group.
7. Wait until the database status becomes **Available**.
8. Copy the RDS endpoint.
9. Open the web application using the provided Web Server IP address.
10. Enter the RDS endpoint, database name, username, and password.
11. Connect the application to the database.
12. Verify the connection by adding, editing, and deleting records in the Address Book application.


## Program

### Security Group Configuration

* Security Group Name: **DB Security Group**
* Inbound Rule: **MySQL/Aurora (3306)**
* Source: **Web Security Group**

### DB Subnet Group

* Name: **DB-Subnet-Group**
* VPC: **Lab VPC**

### Amazon RDS Configuration

* Engine: **MySQL**
* Template: **Dev/Test**
* Availability: **Multi-AZ**
* DB Instance Identifier: **lab-db**
* Username: **main**
* Password: **lab-password**
* Instance Class: **db.t3.micro**
* Storage: **20 GB (General Purpose SSD)**

### Connect the Application

```text
Endpoint : <RDS Endpoint>
Database : lab
Username : main
Password : lab-password
```

After submitting the above details, perform Add, Edit, and Delete operations on the Address Book application.

## Output

<img width="1920" height="1080" alt="Screenshot 2026-11-17 082057" src="https://github.com/user-attachments/assets/364b54a9-5b2d-44fb-b84d-3aab7735628b" />
<img width="1920" height="1080" alt="Screenshot 2026-11-17 082415" src="https://github.com/user-attachments/assets/9e365db0-ac62-4f5f-9bf7-c4915e7aa847" />

<img width="1917" height="720" alt="Screenshot 2026-11-17 082632" src="https://github.com/user-attachments/assets/c8325767-5c25-45d6-a380-72111549e41a" />
<img width="1920" height="1080" alt="Screenshot 2026-11-17 083656" src="https://github.com/user-attachments/assets/414c3050-f17c-4ee3-8572-e9ccc6cc6550" />
<img width="1920" height="1080" alt="Screenshot 2026-11-17 083552" src="https://github.com/user-attachments/assets/aba95000-a98b-4570-9888-98802932bb32" />

<img width="1907" height="904" alt="image" src="https://github.com/user-attachments/assets/f00996c3-9f16-4f0b-9656-b2a9d5a3a4fb" />

## Result

Thus, an Amazon RDS database instance was successfully created and configured as a cloud data storage server. The database was securely connected to a web application, and data operations such as inserting, updating, and deleting records were successfully performed through the application.


