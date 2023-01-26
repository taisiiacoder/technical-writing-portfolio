# Basic concepts

In the section **Management → Users → Accounts**, each user can specify a list of groups to which he belongs.

Group access rights are configured in the administrative panel of the online store in the section **Management → Users → Groups**.

![user_groups1](https://user-images.githubusercontent.com/50182933/214753318-23761ca1-755b-428e-b5e0-2c31722feaa5.jpg)

## List of user groups

There are several system user groups from the beginning, they cannot be deleted:

-   **Guests** - all site visitors automatically belong to this group (the "Guests" group exists only on the client side of the site)
-   **Clients** - authorized users automatically belong to this group (the "Clients" group exists only on the user side of the site)
-   **Administrators** - a group of users with access to the administrative panel of the site
-   **Supervisors** - a group of users with full access to all system functions

To create a new user group, click the "Add" button in the upper left corner.

## User group settings

Basic tab

-   **Nickname (English)** - group identifier (it is impossible to change after the group has been created)
-   **Group** - name for the administrative panel
-   **Description** - textual description of the role of the group
-   **Administrator** - flag whether the group is an administrator

"Permissions" tab (settings on this tab are individual for each multisite)

-   **Enable access to the administration of the current site** - flag, access to the administrative panel of the site
-   **Block "Access to menu items"** - allows you to specify which items will be available to members of this group
-   **Block "Permissions to modules"** - allows you to specify access rights to system modules for members of this group

## Accessing menu items

![access_menu](https://user-images.githubusercontent.com/50182933/214918700-c20be73e-eb3f-4511-8b73-cc34e8fbf0e7.jpg)

The "Access to menu items" block consists of 2 parts:

-   **on the left "user menu"** - client menu, configured in the section **Website → Menu**
-   **on the right "admin menu"** - a menu in the administrative panel, created by modules installed on the site

If a user belongs to several groups at the same time, he gets access to all menu items specified in his groups.

Menu items to which the user does not have access are not displayed in the client part and in the administrative panel.

## Access to modules

![access_module](https://user-images.githubusercontent.com/50182933/214918828-629361d7-23c7-4fd6-ba8d-a7b7382a833d.jpg)

Each module has its own set of rights. For each right, you can specify the access level:

-   **Permission** - the group has access to this right
-   **Prohibited** - the group does not have access to this right
-   **By default** - the group does not affect access to this right

If a user belongs to several groups at the same time, the access rights of his groups are summed up. In this case, if the user's groups have different access to the right or none of the groups affects the right, the access level is determined by **the "Priority of rights" setting** in the **Administration → System settings section → the "Permissions system" tab**.
