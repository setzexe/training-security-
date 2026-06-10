# SQL Injection

SQL Injection is one type of code injection. **Code Injection** is when you can add your own information into a data stream. You can input a command and the terminal might run it server side. This is typically enabled due to bad programming. The application should properly handle input and output.

There is a lot of different types. HTML, XML, so on.

With **SQL** in particular, this is relatively straightforward. This can often happen in the web browser. The application should not allow this, there should be some form of sanitization (sanitizing impure code or intent from input).

A famous SQL injection example is the **' OR 1=1; --**. 
- **'** closes the string the application is meant to look for.
- **OR 1=1** is always true; therefor the query will be true.
- **--** is SQL comment syntax; it will ignore the rest of the original query.

If looking for a user based on an inputted password, adding ' OR 1=1 -- to a query would just showcase every user.

Because this query came back as true, this could be used to view or manipulate the database. Add users, info, delete entire tables, so on so forth.