# Task-Management-System

This is a Task Management System application. It provides the functionality to register users, create tasks, update task details, assign tasks to users, mark tasks as complete, delete tasks, and perform various search and filter operations on tasks.

# Features
  - User Management:

    - User registration: Users can register an account by providing their details.
    - User login: Users can log into their account using their credentials.
    - User logout: Users can log out from their account.

  - Task Management:

    - Create task: Users can create tasks by providing the task details.
    - Update task: Users can update the details of an existing task.
    - Assign task to another user: Users can assign a task to another user.
    - Mark task as complete: Users can mark a task as complete.
    - Delete task: Users can delete a task.

  - Search and Filter:

    - Search task by title: Users can search for tasks based on the task title.
    - Search task by description: Users can search for tasks based on the task description.
    - Search tasks of a user: Users can retrieve all the tasks associated with a specific user.
    - Filter tasks by completion status: Users can filter tasks based on their completion status.
    - Filter tasks by due date: Users can filter tasks based on their due date.
    - Filter tasks by completion status and due date: Users can filter tasks based on their completion status and due date.


# Technologies Used
  - Java
  - Spring Boot
  - Hibernate
  - Maven
  - MySQL
  - HTML
  - CSS
  - JavaScript
  - Bootstrap

# API Endpoints

  - User Endpoints:

    - POST /api/users: Register a new user.
    - POST /api/users/login: Log in to a user account.
    - POST /api/users/logout/{token}: Log out from a user account.

  - Task Endpoints:

    - POST /api/tasks/{token}: Create a new task.
    - PUT /api/tasks/{token}: Update an existing task.
    - PUT /api/tasks/{token}/{taskId}/{userId}: Assign a task to another user.
    - PUT /api/tasks/complete/{token}/{taskId}: Mark a task as complete.
    - DELETE /api/tasks/{token}/{taskId}: Delete a task.

  - Search and Filter Endpoints:

    - GET /api/search/title/{token}/{title}: Search for tasks by title.
    - GET /api/search/desc/{token}/{desc}: Search for tasks by description.
    - GET /api/search/user/{userId}: Retrieve tasks of a specific user.
    - GET /api/filter/completionstatus/{token}/{completedStatus}: Filter tasks by completion status.
    - GET /api/filter/duedate/{token}/{dueDate}: Filter tasks by due date.
    - GET /api/filter/{token}/{completedStatus}/{dueDate}: Filter tasks by completion status and due date.

# Usage Examples

  - User Endpoints:

    - Register a new user:
      - Request: POST /api/users
        ```html
        http://localhost:8080/api/users
        ```
      - Body:
        ```json
        {
            "name":"Sanjan",
            "mobile":"7589614279",
            "username":"Sanjan1",
            "password":"1234"
        }
        ```


        ![register](https://github.com/sanjanyadav420/Task-Management-System-/assets/101393474/404f422f-9151-48e2-9ea4-ffdded70f8f7)

        
        
    -  Log in to a user account:
      

        - Request: POST /api/users/login
          ```html
          http://localhost:8080/api/users/login
          ```
        - Body:
          ```json
          {
              "username":"Sanjan1",
              "password":"1234"
          }
          ```

        ![login](https://github.com/sanjanyadav420/Task-Management-System-/assets/101393474/5a9bac9e-f33f-44fd-abaf-8f861c0e9160)

          
    -  Log out from a user account:
        - Request: POST /api/users/logout/{token}
          ```html
          http://localhost:8080/users/logout/{token}
          ```
     
          
      
  - Task Endpoints:

    - Create a new task:
        - Request: POST /api/tasks/{token}
          ```html
          http://localhost:8080/api/tasks/{token}
          ```
        - Body:
          ```json
          {
              "title":"title",
              "description":"description",
              "dueDate":"2023-07-10",
              "completed":"false"
          }
          ```
![assign](https://github.com/sanjanyadav420/Task-Management-System-/assets/101393474/60c44246-56c2-48b7-af6c-0a13691fdc72)

          
    - Update an existing task:
        - Request: PUT /api/tasks/{token}
          ```html
          http://localhost:8080/api/tasks/{token}
          ```
        - Body:
          ```json
          {
              "title":"title",
              "description":"description",
              "dueDate":"2023-07-10",
          }
          ```

        ![createtask](https://github.com/sanjanyadav420/Task-Management-System-/assets/101393474/1d9e8f22-52f8-4808-8d1b-22436e61f72a)


          
    - Assign a task to another user:
        - Request: PUT /api/tasks/{token}/{taskId}/{userId}
          ```html
          http://localhost:8080/api/tasks/${token}/${taskId}/${userId}
          ```

         ![createtask](https://github.com/sanjanyadav420/Task-Management-System-/assets/101393474/52eba7b8-e2e0-4fe4-9508-6867523ce7bd)


          
    - Mark a task as complete:
        - Request: PUT /api/tasks/complete/{token}/{taskId}
          ```html
          http://localhost:8080/api/tasks/complete/${token}/${taskId}
          ```

![mark](https://github.com/sanjanyadav420/Task-Management-System-/assets/101393474/9d3da36d-9444-4920-88be-f313d5c9f95f)


          
    - Delete a task:
        - Request: DELETE /api/tasks/{token}/{taskId}
          ```html
          http://localhost:8080/api/tasks/${token}/${taskId}
          ```
![delete](https://github.com/sanjanyadav420/Task-Management-System-/assets/101393474/df700759-f7b1-4d41-b9e3-edc3dc12bd3d)


          

  - Search and Filter Endpoints:

    - Search for tasks by title:
      - Request: GET /api/search/title/{token}/{title}
          ```html
          http://localhost:8080/api/search/title/${token}/${title}
          ```

       ![title](https://github.com/sanjanyadav420/Task-Management-System-/assets/101393474/c720ff63-014e-4d00-affa-6e498537ee1b)



          
    - Search for tasks by description:
      - Request: GET /api/search/desc/{token}/{desc}
          ```html
          http://localhost:8080/api/search/desc/${token}/${description}
          ```

         ![filter](https://github.com/sanjanyadav420/Task-Management-System-/assets/101393474/e7e30452-0d7e-4332-8ec7-d3a09f5413a6)


    - Filter tasks by completion status:
      - Request: GET /api/filter/completionstatus/{token}/{completedStatus}
          ```html
          http://localhost:8080/api/filter/completionstatus/${token}/${completedStatus}
          ```


![mark](https://github.com/sanjanyadav420/Task-Management-System-/assets/101393474/9d3da36d-9444-4920-88be-f313d5c9f95f)
     



    - Filter tasks by due date:
      - Request: GET /api/filter/duedate/{token}/{dueDate}
          ```html
          http://localhost:8080/api/filter/duedate/${token}/${dueDate}
          ```

       ![filterdate](https://github.com/sanjanyadav420/Task-Management-System-/assets/101393474/4ca3a585-5b92-46ce-80a9-43b60b606e8e)


