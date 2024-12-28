Automated Shell Script

Here is a Bash script that automates user and group administration on Linux (Ubuntu). It allows for creating and deleting users, creating and deleting groups, and modifying user group memberships.

Bash Script: user_group_admin.sh

Features of the Script:

Create User: Creates a new user, optionally adding the user to a specific group.
Delete User: Deletes an existing user along with their home directory.
Add User to Group: Adds an existing user to a specific group.
Remove User from Group: Removes an existing user from a specified group.
Create Group: Creates a new group.
Delete Group: Deletes an existing group.
List Users: Lists all users in the system.
List Groups: Lists all groups in the system.

Script Details:

create_user: Uses useradd to create a user, optionally adding them to a group.
delete_user: Uses deluser --remove-home to remove a user and their home directory.
add_user_to_group: Uses usermod -aG to add a user to a group.
remove_user_from_group: Uses deluser to remove a user from a group.
create_group: Uses groupadd to create a group.
delete_group: Uses groupdel to delete a group.
list_users: Uses getent passwd to list users.
list_groups: Uses getent group to list groups.

Security Considerations:

The script requires sudo privileges for most commands, so ensure it is run by an authorized user.
Be cautious when running commands that modify system users and groups, as this could affect system stability and access control.

Error Handling:

The script provides basic feedback about each operation, but error handling can be enhanced by checking for specific error codes from the system commands if necessary.

