


## Create User Account using Register

Create an Account for the User if an Account for that particular User does not already exist.

**URL** : ``` /api/signup/ ```

**Method** : ``` POST ```

**Auth required** : NO

**Permissions required** : None

**Data constraints:**

```
{
    "Firstname": "[not null]",
    "Lastname": "[not null]",
    "email": "[must be unique,not null]",
    "password": "[not null]",
}
```
| Parameter      | Description
| :---        |    ----:  
| Firstname      | first name of user      
| Lastname   | last name of user     
| Email      |email of user        
| password      | password of user |

Data Examples for user
```
{
    "Firstname": "[abcde]",
    "Lastname": "[xyz]",
    "email": "[abcde@ufl.edu]",
    "password": "[12345]",
}
```
| Parameter      | Sample Input 
| :---        |    ----:  
| Firstname      | abcde      
| Lastname   | xyz     
| Email      |abcde@ufl.edu     
| password      | 12345      
## Success Response

Condition : If everything is OK and an Account didn't exist for this User.
Code : 201 SUCCESS

## Error Responses
Condition : If Account already exists for User, which include two situation: username or email already exists.

Code : 400 BadRequest

Content : {"error": "Could Not Login!"}
