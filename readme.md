| Container Name | Image Used                      | Port       | Username | Password |
| -------------- | ------------------------------ | ---------- | -------- | -------- |
| postgres       | postgres:latest                | 5439:5439  | postgres | 1234     |
| mongomoviescontenedor | mongo                   | 27018:27017 | usrmongo | pwdmongo |
| mongobillscontenedor | mongo                   | 27019:27017 | usrmongo | pwdmongo |
| mongousercontenedor  | mongo                   | 27020:27017 | usrmongo | pwdmongo |
| local_keycloak | quay.io/keycloak/keycloak:18.0.2 | 8080:8080  | admin    | admin    |

Users Microservice
| Endpoint | Method | Description |
| --- | --- | --- |
| http://localhost:9090/api/users | GET | Retrieve all users (requires authentication) |
| http://localhost:9090/api/users/{id} | GET | Retrieve user by id (requires authentication) |
| http://localhost:9090/api/users | POST | Create new user (requires authentication) |
| http://localhost:9090/api/users/{id} | PUT | Update user by id (requires authentication) |
| http://localhost:9090/api/users/{id} | DELETE | Delete user by id (requires authentication) |

