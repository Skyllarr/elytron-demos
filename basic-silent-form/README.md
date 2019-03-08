## Demo web app for BASIC authentication in SILENT mode 

### Run and configure wildfly:

Run wildfly server and then move to source folder of this example. To configure elytron:
```
{path_to_wildfly}/bin/jboss-cli.sh --connect --file=configure.cli
```

Above batch configured BASIC authentication in SILENT mode and FORM based authentication.

To deploy this demo run:

```
mvn clean install wildfly:deploy
```

#### Now you can access this demo in your browser at [http://localhost:8080/basic-silent](http://localhost:8080/basic-silent) 

User can authenticate with FORM based auth (Note: the browser did not create authentication pop up, because the challenge was not sent by the server).
To login: **user** with password **password**

It is also possible to login with BASIC authentication if the request is sent with Authorization header and above credentials encoded in Base64. 
(I suggest trying this with tools like curl, Postman etc.)
