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

Email setup (SendGrid): https://app.sendgrid.com/guide/integrate/langs/nodejs
		https://app.sendgrid.com/guide/integrate/langs/nodejs/verify



		TODO: fix this error 


			2023-01-02T17:42:17.162782+00:00 heroku[web.1]: State changed from starting to up
2023-01-02T17:42:16.947200+00:00 app[web.1]: Warning: connect.session() MemoryStore is not
2023-01-02T17:42:16.947207+00:00 app[web.1]: designed for a production environment, as it will leak
2023-01-02T17:42:16.947207+00:00 app[web.1]: memory, and will not scale past a single process.
2023-01-02T17:42:16.956152+00:00 app[web.1]: Listening on port: 34056
2023-01-02T17:42:10.000000+00:00 app[api]: Build succeeded
2023-01-02T17:42:10.330261+00:00 app[api]: Deploy d5cfa544 by user aronprenovostmktg@gmail.com
2023-01-02T17:42:17.590013+00:00 app[web.1]: ResponseError: Forbidden
2023-01-02T17:42:17.590027+00:00 app[web.1]:     at node_modules/@sendgrid/client/src/classes/client.js:146:29
2023-01-02T17:42:17.590028+00:00 app[web.1]:     at process.processTicksAndRejections (node:internal/process/task_queues:95:5) {
2023-01-02T17:42:17.590028+00:00 app[web.1]:   code: 403,
2023-01-02T17:42:17.590029+00:00 app[web.1]:   response: {
2023-01-02T17:42:17.590029+00:00 app[web.1]:     headers: {
2023-01-02T17:42:17.590029+00:00 app[web.1]:       server: 'nginx',
2023-01-02T17:42:17.590030+00:00 app[web.1]:       date: 'Mon, 02 Jan 2023 17:42:17 GMT',
2023-01-02T17:42:17.590030+00:00 app[web.1]:       'content-type': 'application/json',
2023-01-02T17:42:17.590030+00:00 app[web.1]:       'content-length': '281',
2023-01-02T17:42:17.590031+00:00 app[web.1]:       connection: 'close',
2023-01-02T17:42:17.590031+00:00 app[web.1]:       'access-control-allow-origin': 'https://sendgrid.api-docs.io',
2023-01-02T17:42:17.590031+00:00 app[web.1]:       'access-control-allow-methods': 'POST',
2023-01-02T17:42:17.590032+00:00 app[web.1]:       'access-control-allow-headers': 'Authorization, Content-Type, On-behalf-of, x-sg-elas-acl',
2023-01-02T17:42:17.590032+00:00 app[web.1]:       'access-control-max-age': '600',
2023-01-02T17:42:17.590032+00:00 app[web.1]:       'x-no-cors-reason': 'https://sendgrid.com/docs/Classroom/Basics/API/cors.html',
2023-01-02T17:42:17.590032+00:00 app[web.1]:       'strict-transport-security': 'max-age=600; includeSubDomains'
2023-01-02T17:42:17.590032+00:00 app[web.1]:     },
2023-01-02T17:42:17.590033+00:00 app[web.1]:     body: { errors: [Array] }
2023-01-02T17:42:17.590033+00:00 app[web.1]:   }
2023-01-02T17:42:17.590033+00:00 app[web.1]: }
2023-01-02T17:42:10.330261+00:00 app[api]: Release v24 created by user aronprenovostmktg@gmail.coms



