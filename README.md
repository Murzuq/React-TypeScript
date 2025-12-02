# React + TypeScript Learning Project

This project is a hands-on learning exercise to understand and practice the integration of TypeScript with React. It serves as a foundational boilerplate for building type-safe, scalable web applications.

## 🚀 Overview

The primary goal of this project is to explore the core concepts of React while leveraging the power of TypeScript for static typing. This includes:

- Setting up a React development environment with TypeScript.
- Creating functional components with typed props and state.
- Understanding how to handle events in a type-safe manner.
- Structuring a React application for clarity and maintainability.

## ✨ Features

- **Type-Safe Components**: All components are built with TypeScript to ensure prop and state types are checked at compile time.
- **Modern React**: Utilizes modern React features like Hooks (`useState`, `useEffect`, etc.).
- **Create React App Boilerplate**: Bootstrapped with Create React App for a streamlined development experience.

## 🛠️ Technologies Used

- React
- TypeScript
- Create React App
- HTML5 & CSS3

## ⚙️ Getting Started

Follow these instructions to get a copy of the project up and running on your local machine for development and learning purposes.

### Prerequisites

Make sure you have the following installed on your system:

- Node.js (v16.x or later recommended)
- npm or yarn

### Installation

1.  Clone the repository to your local machine:

    ```sh
    git clone https://github.com/Murzuq/React-TypeScript.git
    ```

2.  Navigate into the project directory:

    ```sh
    cd react-typescript
    ```

3.  Install the dependencies:
    ```sh
    npm install
    ```
    or if you use yarn:
    ```sh
    yarn install
    ```

### Running the Application

To start the development server and view the application in your browser:

```sh
npm start
```

or

```sh
yarn start
```

This will open the application at http://localhost:3000. The page will automatically reload if you make edits.

## 📂 Project Structure

The project follows a standard Create React App structure:

```
react-typescript/
├── public/
│   ├── index.html      # The main HTML page
│   └── ...
├── src/
│   ├── components/     # Reusable components (optional, but good practice)
│   ├── App.tsx         # The main application component
│   ├── index.tsx       # The entry point of the application
│   └── react-app-env.d.ts # TypeScript declarations for CRA
├── package.json
└── tsconfig.json       # TypeScript configuration
```

## 🧠 Learning Goals

This project aims to cover the following concepts:

- **Component Typing**: Defining interfaces for component props (`React.FC<Props>`).
- **State Management**: Using the `useState` hook with explicit types.
- **Event Handling**: Typing event handlers for forms, buttons, and other interactive elements.
- **Project Configuration**: Understanding the roles of `tsconfig.json` and how it works with a React project.

## 💡 Key Concepts Learned

Throughout this project, I have gained a better understanding of:

- **Typed Component Props**: How to define an `interface` or `type` for component props. This ensures that components receive the correct data types, preventing common bugs and improving developer experience with autocompletion.

  ```typescript
  interface GreetingProps {
    name: string;
  }

  const Greeting: React.FC<GreetingProps> = ({ name }) => {
    return <h1>Hello, {name}</h1>;
  };
  ```

- **State Management with `useState`**: How to use the `useState` hook with explicit types. TypeScript can often infer the type, but for complex state, providing a type argument (e.g., `useState<User | null>(null)`) is crucial for type safety.

  ```typescript
  const [count, setCount] = useState<number>(0);
  ```

- **Typed Event Handling**: How to correctly type event handlers for DOM events. This prevents errors when accessing event properties and provides clarity on what kind of event is being handled.
  ```typescript
  const handleClick = (event: React.MouseEvent<HTMLButtonElement>) => {
    // `event` is fully typed
  };
  ```
