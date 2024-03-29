# GitFlow Workflow for DeliverIT

Our team will be using the GitFlow workflow for managing the development and maintenance of our application, DeliverIT as a solution to the problem of maintaining a software project in which several developers or teams are collaborating.

## Branching Strategy

Our repository will have two main branches with an infinite lifetime:

1. **Main**: This branch will contain the official release history, and each commit on this branch will represent a new production release. All the code in the master branch is deployable and is essentially production-ready.

2. **Develop**: This branch serves as an integration branch for features. It contains the complete history of the project, whereas main contains an abridged version. All the code in the develop branch is in a beta state, testable and runnable, but not necessarily production-ready.

In addition to these main branches, we will maintain various support branches:

- **Feature branches**: These branches are used to develop new features for the upcoming or a distant future release. When starting development of a feature, the target release in which this feature will be incorporated may well be unknown at that point. The essence of a feature branch is that it exists as long as the feature is in development, but will eventually be merged back into develop or discarded.

- **Bugfix branches**: These branches are used to prepare code fixes for the upcoming or a distant future release. They allow for minor bug fixes and preparing meta-data for a release (version number, build dates, etc.). By doing all of this work on a bugfix branch, the develop branch is cleared to receive features for the next big release.

- **Hotfix branches**: These branches are very much like bugfix branches in that they are also meant to prepare for a new production release, albeit unplanned. They arise from the necessity to act immediately upon an undesired state of a live production version. When a critical bug in a production version must be resolved immediately, a hotfix branch may be branched off from the corresponding tag on the master branch that marks the production version.

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.

test

# GitFlow Workflow for DeliverIT

Our team will be using the GitFlow workflow for managing the development and maintenance of our application, DeliverIT as a solution to the problem of maintaining a software project in which several developers or teams are collaborating.

xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx


# Project description

## Project Repository about a Package Distribution Application

This project is about an application for a package distribution company that manages delivery drivers responsible for distributing packages. Each driver will receive a certain number of packages during the day to be delivered to customers with different addresses.

The application will have the presence of two main roles:

- **Package Delivery Driver Role**: This role is responsible for receiving the package delivery requests for the day and has the freedom to choose the order of delivery.

- **Administrator Role**: The administrator role is responsible for:
  - Assigning/reassigning packages.
  - Editing delivery addresses.
  - Monitoring the delivery of packages by the drivers throughout the day.


## Back-End

The project named  **deliverit-back**  uses Express, NodeJs, Typescript, and configuration files necessary for the application to work with Docker.

Our team performed various tests to ensure that the "deliverit-front" repository is functioning and ready to start developing functionalities for the next sprint.



## Back-end folder structure

- `.github/workflows/`: 
  - `push.yml`
  - This folder contains GitHub Actions workflows and the file defines the actions to be performed when pushing changes to the repository.
- `.husky/`: 
  - `.gitignore`
  - `husky.sh`
  - `precommit`
  - This folder is for Husky, that allows to add Git hooks to our project.
- `config/`: 
  - For configuration files.
- `dist/`: 
  - Folder generated when we build our project, and it contains the files necessary to run the system on a server.
- `public/images/`: 
  - For images. 
- `src/`: 
  - `controllers/`: 
    - The controllers handle the logic of our application.
  - `middlewares/`: 
    - This folder is intended for the middlewares which are functions that are executed before the controllers.
  - `models/`: 
    -  for the models of our project, which represent the data of our application.
  - `repositories/`: 
    - They're repositories of your project, which handle the communication with the database.
  - `routes/`: 
    - This folder is intended for the routes of our project, which define the endpoints of our API.
  - `services/`: 
    -  For the services of your project, which handle the business logic of our application.
- `tests/`: 
  - This folder is intended for the tests of our project.

xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx

# Project description

## Project Repository about a Package Distribution Application

This project is about an application for a package distribution company that manages delivery drivers responsible for distributing packages. Each driver will receive a certain number of packages during the day to be delivered to customers with different addresses.

The application will have the presence of two main roles:

- **Package Delivery Driver Role**: This role is responsible for receiving the package delivery requests for the day and has the freedom to choose the order of delivery.

- **Administrator Role**: The administrator role is responsible for:
  - Assigning/reassigning packages.
  - Editing delivery addresses.
  - Monitoring the delivery of packages by the drivers throughout the day.

- **This front-end repository is only intended for the functionalities of the "Package Delivery Driver Role"**


## Front-End


The project named  **deliverit-front** uses NextJs as the framework, along with selected languages, libraries, and frameworks such as Typescript, React, and Tailwind. Configuration files necessary for the application to work with Docker have also been added.

Our team performed various tests to ensure that the "deliverit-front" repository is functioning and ready to start developing functionalities for the next sprint.



## Front-end folder structure



- .github/workflows   
  - push.yml
    - This folder contains GitHub Actions workflows and the file defines the actions to be performed when pushing changes to the repository. 
- .husky/
  - .gitignore.yml
  - .husky.sh
  - precommit
    - This folder is for Git configuration in the project and it contain files that automate certain Git tasks.  
- adapters/
    - Contain adapters, which are modules responsible for interacting with external services or APIs. 
- app/
    - This folder represents the main application code. 
  - (PrincipalFlow)/
    - This subfolder represents the main flow of the application and contains the subfolders  home/, on course/, and packages/, which likely correspond to different pages or sections of the application.
 
    - home/
    - on course/
    - packages/
  - (User)/
    - This subfolder represents the user-related functionality of the application.  
    - login
    - signup
- components/
    - This folder contains reusable components that can be used throughout the application.
    - commons/
    - ui/
- hooks/
    - This folder may contain custom React hooks.
- interceptors/
    - This folder may contain interceptors, which are modules responsible for intercepting and modifying requests or responses in an application. Interceptors are commonly used for tasks such as authentication, error handling, or data transformation. 
- interfaces/
    - This folder contains TypeScript interface definitions.
- public/
    - This folder contains static files that can be accessed by the user, such as images, fonts, or other assets. 
- redux/
    - This folder may contain files related to state management using Redux.  It may include actions, reducers, and selectors for managing and accessing global state.
- services/
    - This folder may contain service modules that handle communication with external APIs or perform other backend-related tasks. Services typically encapsulate API calls and provide an interface for interacting with external resources.
- styles/
    - It contains global styles for the application, for example the font-family for the body.
- utils/
    - contain utility functions or helper modules that provide common functionality used throughout the application.

xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx


