Project completed as a part of CodeAcademy's course - "OWASP Top 10: Injection Attacks!".

Original web form was vulnerable to SQL injections and lacked input santization. 

'app.js' is the hardened code that includes prepared statements and input santization using the predefined SQL table references (EMPLOYEE, EMPLOYEEID)
  
  As can be deduced from the SQL table references, this returns employee information demonstrated by consistent corporate email addresses (@chinookcorp) and locations (Calgary, AB, Canada)
  
'app1.js' is the same hardened code using updated SQL table_names (Customer, CustomerID)
  
  This returns what is more likely customer information as the email addresses and locations of identities returned are varied
  
  Interestingly, while inputting different integers to the Customer ID field returns unique results, the Customer ID is undefined for each profile on output.

'specapp.js' contains specific query parameters that reference the relevant information for the customer address

This project is a useful beginner's project in becoming familiar with input santization and SQL database queries.

  I spent some time playing around with the SQL query parameters to explore what works and what doesn't. I would recommend you do the same in completing the project.

  In practice, this is still an insecure node as any user can query the database for all addresses on file.

  Practical applications should require users to be validate their identity and allow restricted access to personal information on file, limited to their own. 
