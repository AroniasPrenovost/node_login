### Project Components

* NodeJS - https://nodejs.org/
* Express - https://expressjs.com/
* MySQL - https://dev.mysql.com/downloads/mysql/
  - no ORM
  - default port 3306
* MySQL Workbench - https://www.mysql.com/products/workbench/

### Project Setup

**1.** Configure .env file for MySQL database connection.
```
cp .env-sample .env
``` 

**2.** Install the below Node.js packages via command line.
```
npm install -g nodemon --save
npm install nunjucks --save
npm install express --save
npm install express-session --save
npm install mysql --save
npm install nodemailer --save
npm install uuid --save
npm install node-fetch@2 --save
```

**3.** Execute the `node_login.sql` file in MySQL Workbench. The SQL file includes a member and admin account for testing purposes.


**4.** If you're using Windows, you can click the `Start_Server_(Windows).bat` file that is included. If not, execute the following in command line: 
```
nodemon --use_strict main.js
```

**5.** Start the server
```
node main.js
```

**6.** If you've successfully started the server, you can navigate to http://localhost:{PORT}/ in your browser. It should take you to the login form.

### Admin Panel

URL: http://localhost:{PORT}/admin/

### Email Setup

**Q:** Why am I not receiving the activation email?\
**A:** You need a working SMTP mail server and make sure your firewall is not blocking ports `25`, `58`, `465`, `110`, etc. This shouldn't be a problem on most hosting providers or Linux servers (built-in email server).

**Q:** Why am I receiving a MySQL error?\
**A:** Make sure you update the MySQL details in the "main.js" file. You might need to change the hostname if yours is different and/or port number, and make sure you've executed the correct SQL file in MySQL Workbench.

**Q:** How do I download the zip file again if I've deleted it?\
**A:** You can request a new receipt email - https://codeshack.io/receiptresend/.

### References 
Based on this tutorial https://codeshack.io/basic-login-system-nodejs-express-mysql/
