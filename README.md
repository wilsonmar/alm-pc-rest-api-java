The current state of this is as it was forked from 
Create, read, update, and delete entities on the ALM HP platform.

Additional coding TODO:
1. Make this run in console mode after Maven install, with default configuration (list projects).
2. Define ALM server userid/password credentials as enviornment variables so they can be managed by Jenkins/Hashicorp Vault.
3. Add Performance Center calls
4. Add output to CSV, MySQL

### Installing
```
mvn clean install
```

### Examples
Here is a simple example that login, returns a test entity and logout from ALM server.
```java
Client client = new Client(new Config("alm.properties"));

client.login();

// Get the test set with specified ID
TestSet testSet = client.loadTestSet("1");

client.logout();
```

### REST API Overview
http://alm-help.saas.hpe.com/en/12.50/api_refs/REST_TECH_PREVIEW/ALM_REST_API_TP.html

### Licensing
See [LICENSE](https://github.com/okean/alm-rest-api/blob/master/LICENSE)
