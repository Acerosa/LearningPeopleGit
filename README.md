# 🏃🏿‍♀️‍➡️ React Exercise – Message Changer Component

Welcome! In this exercise, you'll create your **first custom React component** that changes text on the screen when a button is clicked.🫵🏿 

By the end, you’ll understand how to:
- Use **state** to store data inside a component  
- Handle **button clicks** to update that state
- Import and use your component inside `App.jsx`

---

## 🎯 Objective

Create a new component that displays a message and a button.  
When the button is clicked, the message changes.

---

## 🪜 Steps

### 1️⃣ Create the component file
1. Inside the **`src`** folder, create a folder named **`components`**.  
2. Inside that folder, create a file name it something that makes sense i.e **MessageChanger**:

![App Preview](public/images/message.png)
## Don't forget to export it
``` jsx
export default MessageChanger;
```

### Use your component in App.jsx
Import the component at the top of App.jsx:

``` jsx
import MessageChanger from "./components/MessageChanger";

const App = () => {
  return (
    <div>
      <h1>🌟 React Lesson – Components</h1>
      <MessageChanger />
    </div>
  );
};

export default App;

```
### 4️⃣ Run & test
- Use **Preview**.  
- Verify that the button successfully changes the message when clicked.

---

## ➕ Bonus Challenges (Optional)

Once your main component works, try these extensions to practise more advanced concepts.

### 🆕 Challenge 1: Add a Reset Button
- Add a second button that restores the original message when clicked.  
- You’ll need to keep a reference to the initial message.

---

### 🔁 Challenge 2: Toggle Between Two Messages
- Make a single button that switches back and forth between two different messages.  
- Use conditional logic to decide which message to show based on the current state.

---

### 🧭 Challenge 3: Use Props to Customise the Starting Message
- Update your component so it can receive a **prop** called `initialMessage`.  
- The component should display whatever message is passed from `App.jsx` when it first loads.  
- Try creating multiple `<MessageChanger />` components in `App.jsx`, each starting with a different message.

---

## 📋 Key Concepts You’re Practising
- Component creation and import  
- React **state** (`useState`)  
- Event handling (`onClick`)  
- Conditional rendering  
- Passing and using **props**

---

## 🛟 Need Help?
1. Click **Share → Live Session → Copy Link**
2. Send that link to your instructor.
3. Wait for live support (we can code together in real time).

---

Enjoy building your first interactive React component! 🧱
