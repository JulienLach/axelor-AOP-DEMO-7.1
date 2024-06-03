# Open Platform Demo

Open Platform Demo is a simple application showing [Axelor Open Platform](https://github.com/axelor/axelor-open-platform) features.

## Installation

Make sure you have JDK 11 and Git installed.

Clone the latest sources:

```bash
$ git clone git@github.com:axelor/open-platform-demo.git
```

and build the project:

```bash
$ cd /path/to/open-platform-demo
$ ./gradlew -x test build
```

This should generate the war package for under build/libs directory. You can test the war by deploying on your tomcat server.

You can also test the application using the embedded tomcat server. First edit the `axelor-config.properties` and configure the database to use and then run the following command from the interactive shell.

```
# PostgreSQL
db.default.driver = org.postgresql.Driver
db.default.ddl = update
db.default.url = jdbc:postgresql://localhost:5432/open-platform-demo-dev-7-1-0
db.default.user = myuser
db.default.password = mypassword
```

```bash
$ ./gradlew --no-daemon run
```

The application should start printing some logs in your terminal window. After few seconds, you should see something like this:
```bash
...
Ready to serve...

Running at http://localhost:8080/open-platform-demo
```

Launch the browser and open the application url as printed on terminal. Use the default **admin/admin** as the user name and password. You should be in the application.