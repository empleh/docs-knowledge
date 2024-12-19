# Files and Folders

Naming files and folders consistently and logically is important. I have found these rules helpful for how to think about that.

## Projects

Projects should have a separate contracts project.

- The Interfaces, Requests, Responses, Models, and Dtos should be in the contracts project.
  - Managers Project would have Managers.Contracts project
- Each interface should have its own Folder.
  - INotificationManager would be in the Notifications folder and a top-level file in that folder.

### Example

In this example the profile models are data used by the client layer and likely a subset of UserDTO data. UserDTO would likely be the same for both Adults and Children.

- **Solution Root**
  - **Managers**
    - **User**
      - **StoreProfile**
        - StoreAdultProfileHandler.cs
        - StoreChildProfileHandler.cs
      - **GetProfile**
        - GetAdultProfileHandler.cs
        - GetChildProfileHandler.cs
    - UserManager.cs 
  - **Managers.Contracts**
    - **User**
      - **Profile**
        - **Models**
          - AdultProfileModel.cs
          - ChildProfileModel.cs
        - **Requests**
          - StoreAdultProfileRequest.cs
          - StoreChildProfileRequest.cs
        - **Responses**
          - StoreAdultProfileResponse.cs
          - StoreChildProfileResponse.cs
    - IUserManager.cs
  - **Accessors**
    - **Users**
      - UserAccessor.cs 
  - **Accessors.Contracts**
    - **Users**
      - **DTOs**
        - UserDto.cs
      - **Filters**
        - UserFilter.cs
      - **Outputs**
        - UserOutput.cs
    - IUserAccessor.cs