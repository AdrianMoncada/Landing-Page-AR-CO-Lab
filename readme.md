| Container Name | Image Used                      | Port       | Username | Password |
| -------------- | ------------------------------ | ---------- | -------- | -------- |
| postgres       | postgres:latest                | 5439:5439  | postgres | 1234     |
| mongomoviescontenedor | mongo                   | 27018:27017 | usrmongo | pwdmongo |
| mongobillscontenedor | mongo                   | 27019:27017 | usrmongo | pwdmongo |
| mongousercontenedor  | mongo                   | 27020:27017 | usrmongo | pwdmongo |
| local_keycloak | quay.io/keycloak/keycloak:18.0.2 | 8080:8080  | admin    | admin    |

Users Microservice

| HTTP Method | Endpoint | Role | Description | Tested |
|-------------|----------|------|-------------|--------|
| GET         | /users/all | ROLE_admin | Get a list of all users | No    |
| GET         | /users/id/{id} | ROLE_admin | Get a user by ID | Yes    |
| POST        | /users/save | ROLE_admin | Create or update a user | No    |
| GET         | /users/admin | ROLE_admin | Get a list of all users except the ones with the role ROLE_admin in Keycloak | Yes    |

> Note: All endpoints can only be accessed through a gateway running on port 9090 and require a valid Keycloak access token with the corresponding roles.



