# Files and Folders

Naming files and folders consistently and logically is important. I have found these rules helpful for how to think about that.

## Projects

Projects should have a separate contracts project.

- The Interfaces, Requests, Responses, Models, and Dtos should be in the contracts project.
  - Managers Project would have Managers.Contracts project
- Each interface should have its own Folder.
  - INotificationManager would be in the Notifications folder and a top-level file in that folder.

### Example

- **Solution Root**
  - **Managers**
    - **Notifications**
      - NotificationManager.cs 
  - **Managers.Contracts**
    - **Notifications**
      - INotificationManager.cs
  - **Accessors**
    - **Users**
      - UserAccessor.cs 
  - **Accessors.Contracts**
    - **Users**
      - IUserAccessor.cs