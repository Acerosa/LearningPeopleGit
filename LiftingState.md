# 🌓 Theme Toggle Dashboard  
**React Project – State Lifting & Controlled Data Flow**

---

## 🎯 Project Objective

In this project, you will build a small React application to practise **state lifting** and **controlled, one-way data flow**.

By the end of this task, you should be able to:
- Identify where shared state should live
- Pass data **down** using props
- Send actions **up** using callback functions
- Explain why React enforces one-way data flow

---

## 🧠 Key Rule (Read This First)

> **If more than one component needs the same data, that data must live in their closest common parent.**

---

## 🏗️ Component Structure

You must create the following structure:
```
src/
├── App.jsx
├── ThemePreview.jsx
└── ThemeToggle.jsx
```

- `App` → owns the theme state
- `ThemePreview` → displays the current theme
- `ThemeToggle` → requests theme changes

---

## 🎨 Theme Requirements

The theme must be one of the following values:
- `"light"`
- `"dark"`

The UI must visually change when the theme changes.

---

## 🧩 Step 1 — App (State Owner)

1. Create a `theme` state in `App` using `useState`
2. Initialise the theme to `"light"`
3. Create a function that toggles the theme between `"light"` and `"dark"`
4. Pass:
   - The current theme **down** to both child components
   - The toggle function **down** to `ThemeToggle`

⚠️ **Important:**  
The theme state must live **only** in `App`.

---

## 🧾 Step 2 — ThemePreview (Display Only)

1. Create a `ThemePreview` component
2. Receive `theme` as a prop
3. Display:
   - The current theme name
   - A preview box whose colours change based on the theme
4. Do **not** create state in this component

> This component must be **read-only**

---

## 🎮 Step 3 — ThemeToggle (Actions Only)

1. Create a `ThemeToggle` component
2. Receive:
   - `theme`
   - A callback function from `App`
3. Add a button that toggles the theme when clicked
4. Do **not** update the theme directly

> This component must request changes using the callback function.

---

## 🔄 Expected Data Flow
```
User clicks button
↓
ThemeToggle calls callback
↓
App updates theme state
↓
App re-renders
↓
ThemePreview updates automatically
```

This is **controlled, one-way data flow**.

---

## 🚫 Rules & Constraints

- ❌ No duplicate theme state
- ❌ No state in child components
- ❌ No direct child-to-child communication
- ✅ One source of truth in `App`

---

This is **controlled, one-way data flow**.

---

## 🚫 Rules & Constraints

- ❌ No duplicate theme state
- ❌ No state in child components
- ❌ No child-to-child communication
- ✅ One source of truth in `App`

---

## 🧪 Your Task

Use the **starter code below** and complete the TODOs.

---
```css
    padding: "16px",
    borderRadius: "8px",
    border: "1px solid #ccc",
    marginTop: "12px",
    backgroundColor: theme === "dark" ? "#111" : "#f5f5f5",
    color: theme === "dark" ? "#fff" : "#111",
```

### boilerplate Code

##### 📁 `src/App.jsx`

```jsx
import { useState } from "react";
// import ThemePreview from "./ThemePreview";
// import ThemeToggle from "./ThemeToggle";

const App = () =>  {
  // TODO:
  // 1. Create state to store the current theme ("light" or "dark")
  // 2. Initialise the theme to "light"

  // TODO:
  // 3. Create a function that toggles the theme between "light" and "dark"

  return (
    <div>
      <h1>Theme Toggle Dashboard</h1>

      {
/* 
        TODO:
        - Pass the current theme to ThemePreview

         <ThemePreview />
      */
}
      

     { /*
        TODO:
        - Pass the current theme to ThemeToggle
        - Pass the toggle function to ThemeToggle
         <ThemeToggle />
         */
}
 
    </div>
  );
}

export default App;

```
![Import](https://raw.githubusercontent.com/Acerosa/LearningPeopleGit/LiftingStateDarkMode/app.png)

-----

##### `src/ThemePreview.jsx`

```jsx
const ThemePreview = (props) => {
  // TODO:
  // 1. Read the theme value from props
  // 2. Create styles that change based on the theme
  //    - light theme: light background, dark text
  //    - dark theme: dark background, light text

  return (
    <div>
      {/* 
        TODO:
        - Display the current theme
        - Show a preview box that visually reflects the theme
      */}
    </div>
  );
}

export default ThemePreview;
```
![Import](https://raw.githubusercontent.com/Acerosa/LearningPeopleGit/LiftingStateDarkMode/ThemePreview.png)

------
##### `src/ThemeToggle.jsx`

```jsx
const ThemeToggle = (props) => {
  // TODO:
  // 1. Read the theme value from props
  // 2. Read the toggle function from props

  return (
    <div>
      {/*
        TODO:
        - Display the current theme
        - Add a button that calls the toggle function when clicked
      */}
    </div>
  );
}

export default ThemeToggle;
```
![Import](https://raw.githubusercontent.com/Acerosa/LearningPeopleGit/LiftingStateDarkMode/ThemeToggle.png)

