# DPS: Data Provider Service

## Description

A specification for a service fetching data. This service fetches the data and manages cache for you it also provides the methods for generating fake data or seeding it if needed.
## Definition

### [single || multiple].getBy{Field}(field)

Fetches the data using the specified field.

Example
```
userEMS.single.getByName("Fred") -> User;

userEMS.single.getById("#42:0") -> User;

userEMS.multiple.getByName("Fred") -> [User]
```

### single.get()

Fetches the default data. For example the User himself

Example:
```
userEMS.single.get() -> User
```

### multiple.get()

Fetches the default data. For example the entire list of all the users.

Example:
```
userEMS.multiple.get() -> [User]
```