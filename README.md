## Task
Your task it to build a full-stack "Todo" Application in TypeScript. There are two discrete components to this system: A web client that will allow the user to interact with the application and a back-end API that the web client interacts with to store and retrieve data. Each component should run in its own process, however the entire project should be contained in a single git repository. The system does not need to support multiple users or persist data between application restarts though several bonus tasks including adding data persistence are outlined in the sections below. The final step is packaging the application in a manner that makes starting the application in development mode easy. Work on this project at your own discretion. The completed version should take no longer than 6 hours to produce but will take significantly less for candidates familiar with the required toolchain.

The two models you will need are provided:

```.ts
enum TodoStatusEnum {
  Active = 'Active', // the todo has is not completed
  Inactive = 'Inactive', // the todo is completed
  Archived = 'Archived', // the todo is archived (bonus)
}

interface Todo {
  title: string; // the title of the todo
  status: TodoStatusEnum; // the status of the todo
  lastUpdatedAt: number // a unix timestamp representing the time the todo was last updated
  createdAt: number; // a unix timestamp representing the time the todo was created
}
```

### Getting Started
Fork this repository into your GitHub account. When you are finished, make a pull request back to this repository. Include a short summary of your experience completing this project in the pull request description. 

## Front-end Application
The front-end should run as its own process. You're free to bootstrap the project however you like, but we recommend using a tool like [create-react-app](https://github.com/facebook/create-react-app). The front-end should make HTTP requests to the backend to retrieve, create, and update todos. Your application will be graded on the following criteria:

### Requirements
- [ ] The user can create a todo with a title via a form.
- [ ] The user can view a table of todos.
- [ ] The user can edit the status and title of a to do via the todo table.
- [ ] The user can delete a todo via the todo table
- [ ] The user can archive a todo (Bonus Task)
- [ ] The user user can view a table of arhchived todos at the `/archived` endpoint (Bonus Task)

### Tools
- [ ] [React](https://github.com/facebook/react) for the view layer
- [ ] [Redux](https://github.com/reduxjs/redux.git) for state management
- [ ] [styled-components](https://github.com/styled-components/styled-components) for CSS
- [ ] [Axios](https://github.com/axios/axios) or [Apollo GraphQL](https://github.com/apollographql/apollo-client) (Bonus Task) for data fetching 


## Back-end Application
The back-end should run as its own process.

### Tools
- [ ] [Express](https://github.com/expressjs/express) or [Koa](https://github.com/koajs/koa)


## Operations Tasks
- [ ] Provide a single `make run` command that will install all dependencies and start the applications
- [ ] Provide a single `make build` command that builds the both the frontend and backend applications into Docker images and tags them as `latest` (Bonus Task)
- [ ] Provide a single `make docker-run` command that builds both applications as Docker containers and runs them in a manner that allows them to communicate (Bonus Task)

