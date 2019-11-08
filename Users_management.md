------------------------------------------------------------------------------
# Tutorial for users management
-----------------------------------------------------------------------------

1. The password file is stored in */etc/passwd*
   
   * Username: Password : User ID : Group ID: Description : Directory : Shell path

2. Configuration for bash shell
   
   .bashrc

3. When users log into system, they expect an environment that can help them be productive. This first program that users encounter is called *shell*. The default user shell in Bash
   
   List of bash shell is stored in: */etc/shells*

4. Encrypted password is stored in */etc/shadow*

5. List of group is stored in */etc/group*

6. List of command to modify and create user, group 

   - Add User and infor
   
   `useradd`

   - Modify user 

   `usermod`

   - Delete user

   `userdel`

   - Add group

  `groupadd`

   - Delete group

  `groupdel`

   - Modify group

   `groupmod`

7. User and Access Pemissions

   (r) read permission

   (w) Write permission

   (x) Execute permission

   (-) No permission or no access

   These permission can be applied to three classes of users:

   Owner

   Group

   Everyone
