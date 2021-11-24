# Python_Database_Connection
#this project connect database to python
import mysql.connector as connector
mydb = connector.connect(host="localhost", user="root" ,passwd="SINGHAM#123")
mycursor=mydb.cursor()
mycursor.execute("show databases")
result = mycursor.fetchall()

