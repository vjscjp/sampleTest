## Users
```
```
##### Users Get
```
```
##### Users Remove
```
```
## Users
```
Users - Manage project users

Commands available for Users:
  Get     Get the current user or all users of a specified project
  Remove  Removes the current user from a project
```
##### Users Get
```
Get the current user or all users of a specified project
Usage: users get [<project>]
  <project> (optional) Project for which to get users; if omitted, gets the current user
Returns either a user struct or an array of user structs
```
##### Users Remove
```
Removes the current user from a project
Usage: users remove <project>
  <project> (required) Project for which to remove the current user
Returns a user struct of the user removed
```
