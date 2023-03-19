| Container Name | Image Used                      | Port       | Username | Password |
| -------------- | ------------------------------ | ---------- | -------- | -------- |
| postgres       | postgres:latest                | 5439:5439  | postgres | 1234     |
| mongomoviescontenedor | mongo                   | 27018:27017 | usrmongo | pwdmongo |
| mongobillscontenedor | mongo                   | 27019:27017 | usrmongo | pwdmongo |
| mongousercontenedor  | mongo                   | 27020:27017 | usrmongo | pwdmongo |
| local_keycloak | quay.io/keycloak/keycloak:18.0.2 | 8080:8080  | admin    | admin    |

Users Microservice
| HTTP Method | Endpoint | Functionality | Required Roles |
| --- | --- | --- | --- |
| GET | /users/all | Get all users | N/A |
| GET | /users/id/{id} | Get user by ID | ROLE_admin |
| POST | /users/save | Save or update user | N/A |
| GET | /users/admin | Get all non-admin users from Keycloak | ROLE_admin |


