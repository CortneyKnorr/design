# EMS: Entity Management Service

## Description

A specification for a service managing a specific entity. This service defines the entity in the context and enable to manipulate and generate entities based on it's own definition

## Definition

### .skeleton
Contains the entity's fields and there default values

> .skeleton[field] = value

Example
```
userEMS.skeleton.authType = local;
```
or
```
userEMS.skeleton = {
    authType: 'local',
    username: undefined,
    password: undefined
};
```

### .enums
Contains the potentital set of values for the different fields  

> .enums[field][value]

Example
```
userEMS.enums.authType.LDAP
```

### .clone(entity: Entity) -> Entity
Clones an entity. Useful to turn an unmutable object into an editable one or by cloning the skeleton.

> .clone(entity: Entity) -> Entity

Example
```
let newUser = userEMS.clone(userEMS.skeleton);
```


