# Frontend-System-Design

In simple terms, Frontend System Design (FSD) is the "master plan" for how a web application is built.
Frontend System Design as the blueprint for building a large-scale web application.

## Why Folder Structure is important

In small folder sturcture does not matter much but in large scale application.

- Scalabality
- Clean Architecture
- Better Team work
- Reuseablity
- Faster Development
- Easy Testing
- Easy Debugging

## Different Type of Folder Stucture

- Layer based Structure(Traditional)

  ![alt text](image.png)
  - Files are grouped by type(Layer) like component services, utils, styles
  - Suitable for small project

- Feature based Structure

  ![alt text](image-1.png)
  - Not suitable for large project

- Hybrid Structure

  ![alt text](image-2.png)
  - Combination of layer based + feature based

## Naming Convention and Documentation

- Easy to maintain
- Team friendly
- You quickly remember what the function or file performing
- Less time spent on understaning the old code
- Faster code fixing
- Code becomees self explaintory
- New developers will understand the purpuse of code quickly
- Avoid duplicacy code

### Folder Naming Rule

- Use lowercase, meaningful and plural names
  - eg. components, images, pages

### File Naming Rules

- Component and Pages files name should be in Pascal case.
  - eg. Header.jsx, LoginForm.jsx
- Non-component files should be in Non-Pascal case.
  - eg. authService.js, applicant.js

### Variable Naming Rules

- Use Camel-case and boolean variable name should start with is, has and can.
  - eg. username, isLoggedIn

### Function Naming Rules

- use Camel-Case and meaningful name
  - eg. calculateTotalPrice();

### Description and Comment Rules

- Always add description and comment for files, function, components. To avoid copy-pasting, for quick understanding of file, function and components
- Always write rule in RULES.md or README.md file
  - ![alt text](image-3.png)
  - ![alt text](image-4.png)
  - ![alt text](image-5.png)

## API Architecture and Service layer

When people talk about API architecture and a service layer in React, they’re really talking about how to organize data fetching, business logic, and communication with backend APIs in a clean, scalable way.

- Separates UI from data logic
- Keeps API calls reusable
- Makes error handling consistent
- Scales as your app grows

A good architecture usually has:
`components → hooks → services → API client → backend`

Benefits:

- Separation of concerns: UI → components (Logic → hooks) API → services
- Reusability: Same API call used across multiple components
- Testability: You can test services independently
- Maintainability: Change API once → updates everywhere

## Centralized API Error handling & Toaster Message

Error should be handled very carefully, so that we need to handle on every page. Create Single Error handler and reuse it to every page.

## Feature Based Routing and Lazy Loading

Feature-based routing in a React frontend system design is a way of organizing routes around features (domains) instead of technical layers (like pages, components, utils). It’s especially useful in large-scale apps where scalability, maintainability, and team ownership matter.
