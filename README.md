# Python_Database_Connection
#this project connect database to python
import mysql.connector as connector
mydb = connector.connect(host="localhost", user="root" ,passwd="SINGHAM#123")
mycursor=mydb.cursor()
mycursor.execute("create database Python_connector")
mycursor.execute("use Python_connector")
mycursor.execute("create table Hospitals(SerialNo int,Hospital_name varchar(50),Doctors int,ward_boys int, nurses int, Beds_Available int)")
mycursor.execute("insert into hospitals(serialno, hospital_name, doctors,ward_boys, nurses, Beds_available) values(1, 'dhanwantari',  50, 30, 70,500)")
mycursor.execute("insert into hospitals(serialno, hospital_name, doctors,ward_boys, nurses, Beds_available) values(1, 'susun',  40, 20, 60,200)")
mycursor.execute("insert into hospitals(serialno, hospital_name, doctors,ward_boys, nurses, Beds_available) values(1, 'bharti',  70, 30, 80,700)")
mycursor.execute("insert into hospitals(serialno, hospital_name, doctors,ward_boys, nurses, Beds_available) values(1, 'singhad',  250, 700, 2000,15000)")
mycursor.execute("insert into hospitals(serialno, hospital_name, doctors,ward_boys, nurses, Beds_available) values(1, 'atharv',  70, 300, 707,5000)")
mycursor.execute("select * from hospitals")
result=mycursor.fetchall()
print(result)
