# useContext

## createContext: 3 Steps
```
// 1. Import createContext
import { createContext, useState } from 'react';

// 2. Create and Export
export const CurrentMessage = createContext(null);

function App() {
  const [message, setMessage] = useState(false);

  return (
    <>
{/* // 3. Establish a provider. What you put inside value is what gets sent out */}
      <CurrentMessage.Provider value={[message, setMessage]}>
        Some Content
      </CurrentMessage.Provider>
    </>
  );
};

export default App;
```

## Question: Why is `currentMessage` capitalized?
The context variable name, `CurrentMessage`, is capitalized because it is a convention in React to capitalize the names of contexts. This is because contexts are essentially `global state`, and global state is typically represented by capitalized variables in React.

Here are some reasons why it is important to capitalize context variable names:

* It makes it clear that the variable is a context, and not just a regular variable.
* It makes it easier to distinguish between contexts and other global state variables.
* It follows the naming convention for global state variables in React.


## useContext: 3 Steps
```
// 1. Import useContext
import { useContext } from "react";

// 2. Import
import { CurrentMessage } from "../App";

export default function Page () {
// 3. Use
  const [message, setMessage] = useContext(CurrentMessage);

  return (
    <>
      <p>{message}</p>
    </>
  )
}
```