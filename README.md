# Node Login App

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

**2.** Install Node.js packages.
```
npm i
```

**3.** Execute the `node_login.sql` file in MySQL Workbench. The SQL file includes a member and admin account for testing purposes.

**4.** Start the server
```
node index.js
```
note: If you're using Windows, you can click the `Start_Server_(Windows).bat` file that is included. If not, execute the following in command line: 
```
nodemon --use_strict index.js
```

**5.** If you've successfully started the server, you can navigate to `http://localhost:{PORT}/` in your browser. It should take you to the login form.

### Admin Panel

URL: `http://localhost:{PORT}/admin/`

### Email Setup

**Q:** Why am I not receiving the activation email?\
**A:** You need a working SMTP mail server and make sure your firewall is not blocking ports `25`, `58`, `465`, `110`, etc. This shouldn't be a problem on most hosting providers or Linux servers (built-in email server).

### References 

Source code: https://codeshack.io/basic-login-system-nodejs-express-mysql/, from https://codeshack.io/

Deployment (Heroku): https://www.raddy.dev/blog/how-to-deploy-node-js-express-ejs-mysql-website-on-heroku-cleardb/

Email setup: https://app.sendgrid.com/guide/integrate/langs/nodejs
