# User 
### Creating a new user in Oracle involves a few steps, including creating the user, assigning privileges, and optionally creating a schema for the user. Here’s a step-by-step guide on how to create a new user in Oracle SQL:

- Step 1: Connect as a Privileged User
  First, you need to connect to Oracle Database as a user with administrative privileges (typically SYS or SYSTEM).

```
CONNECT sys as sysdba;
Enter the password when prompted.
```

- Step 2: Create a New User
  Use the CREATE USER statement to create a new user. Replace new_username and password with your desired username and password for the new user.

```
CREATE USER new_username IDENTIFIED BY password;
```
 - For example, to create a user named new_user with password password123:
   
```
CREATE USER new_user IDENTIFIED BY password123;
```

- Step 3: Grant Privileges
Grant necessary privileges to the new user. For example, to grant CONNECT and RESOURCE roles:

```
GRANT CONNECT, RESOURCE TO new_username;
You can grant other privileges as needed for the user’s specific requirements.
```
- Step 4: Optionally Create a Schema
  
```
If you want the new user to have their own schema, you can create it and optionally set it as the default schema for the user.

CREATE SCHEMA new_schema AUTHORIZATION new_username;
```
Step 5: Exit SYSDBA Mode
After creating the user, you can exit the SYSDBA mode if you no longer need it.

```
EXIT;
```

- Step 6: Connect as the New User
Finally, connect to Oracle Database using the new user credentials to verify the connection.
```
CONNECT new_username/password;
```
Replace new_username and password with the actual username and password you created.

Example in Sequence
Here is an example sequence of commands to create a new user named new_user with password password123, grant necessary privileges, and verify the connection:
```
sql
Copy code
-- Connect as SYSDBA
CONNECT sys as sysdba;

-- Create a new user
CREATE USER new_user IDENTIFIED BY password123;

-- Grant CONNECT and RESOURCE roles
GRANT CONNECT, RESOURCE TO new_user;

-- Optionally create a schema
CREATE SCHEMA new_schema AUTHORIZATION new_user;

-- Exit SYSDBA mode
EXIT;

-- Connect as the new user
CONNECT new_user/password123;
```

### Notes:

- Adjust the privileges (CONNECT, RESOURCE, etc.) and roles according to the specific needs of the new user.
- Always ensure strong password policies and security measures when creating new users.
- The `SYS` user or a user with `DBA` privileges (`SYSDBA` role) is required to create new users and grant privileges.
  
This process should help you create a new user in Oracle SQL effectively. Adjust the statements as per your specific requirements and security policies.

#

## Query the DBA_USERS view:

Once connected, you can query the DBA_USERS view to get a list of all users in the database:

```
SELECT username, account_status, created
FROM dba_users; # or FROM all_users; # or From user_users;
```
This query retrieves the username, account_status (like OPEN, LOCKED, etc.), and created (date when the user was created) for each user in the database.
# 
## Important Notes:
- Access to DBA_USERS and ALL_USERS requires appropriate privileges (SELECT_CATALOG_ROLE or DBA role).
- When querying DBA_USERS, you will see all users across the entire database.
- ALL_USERS shows users visible to your current user session, while USER_USERS shows information specifically about the   current user.
  
By using these queries, you can effectively view all users in an Oracle database and their relevant details such as account status and creation date. Adjust your query based on your specific access and visibility needs within the database environment.
#
# Summary of Differences:

- ALL_USERS: Provides visibility into all users across the entire database that are visible to the current user session, typically requires SELECT_CATALOG_ROLE.

- USER_USERS: Shows information about the user currently logged in, which is useful for self-checking without requiring elevated privileges.

- DBA_USERS: Offers comprehensive information about all users in the database, regardless of current user session, requires DBA role or direct privilege on the view.

These views cater to different needs based on the level of access and information required about users within an Oracle database environment.








