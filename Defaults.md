## Defaults
```
```
##### Defaults Get
```
```
## Defaults
```
```
##### Defaults Get
```
```
## Defaults
```
Defaults - Show and set default IDs
-----------------------------------
The Shipped CLI stores default values in configuration files in project and service directories.  Defaults are stored
automatically by Create commands and explicitly by Set commands.  The Shipped CLI automatically uses a default when
available if a value is unspecified for a required field.  To use a default value for an optional field, specify a value
of a single dollar sign. You can also reference an object by:

- specifying a unique partial Name value, optionally preceded by % if the value could be interpreted as a UUID.
e.g. "service create test PHP name=x" creates a service for an application whose name contains "test" from a buildpack
whose name contains "PHP" (case independent)

- specifying it by unique UUID prefix (Docker style).
e.g. service get 1f3 lists services from the application with an application whose ID begins "1f3"


Commands available for Defaults:
  Get  Get default values
```
##### Defaults Get
```
Get default values
Usage: defaults get
Returns a Defaults struct
```
