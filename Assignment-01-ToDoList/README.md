#  Assignment 01:📝 To-Do List

<p align="center">
  <img src="./assets/display-APP-ezgif.com-speed.gif" width="600" alt="App Demonstration GIF" style="border-radius: 20px; border: 5px solid #696FC7; box-shadow: 0 15px 35px rgba(0,0,0,0.3);" />
  <br>
  <br>
  <strong style="font-size: 18px; color: #696FC7;">(Animated Demo: High-Resolution Application Operations)</strong>
</p>

---

<p align="center">
  <img src="https://img.shields.io/badge/React_Native-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" />
  <img src="https://img.shields.io/badge/Expo_Snack-000020?style=for-the-badge&logo=expo&logoColor=white" />
  <img src="https://img.shields.io/badge/Course-Mobile_Computing-blueviolet?style=for-the-badge" />
</p>

## Live Experience on Expo Snack
You can interact with the live code and run the app directly via the button below:

[![Run on Expo Snack](https://img.shields.io/badge/Run_on_Expo_Snack-000020?style=for-the-badge&logo=expo&logoColor=white)](https://snack.expo.dev/@basma_mohamed/blessed-red-cashew)

---

## 📝 Project Overview
This application is a professional **To-Do List** manager built using **React Native**. Developed within the **Expo Snack** environment, it provides a seamless cross-platform experience with a focus on elegant design and robust state management.

---

## 🎨 Visual Identity & Color Palette
The UI is designed using a sophisticated aesthetic palette curated from **Color Hunt** to ensure visual harmony.

* **Palette Source**: [Color Hunt #696FC7](https://colorhunt.co/palette/696fc7a7aae1f5d3c4f2aebb)
* **Design Colors**:
    * **Header & Primary Buttons**: `#696FC7` (Deep Lavender)
    * **Main Background**: `#F2AEBB` (Peach Pink)
    * **Active Task Cards**: `#A7AAE1` (Soft Purple)
    * **Completed Task State**: `#F5D3C4` (Light Peach)

---

## 📸 Static Preview (High-Resolution Screenshots)

| 1. Initial State | 2. Adding Tasks | 3. Operations (Complete/Delete) |
| :---: | :---: | :---: |
| <img src="./assets/image01.png" width="250" style="border-radius: 10px; border: 2px solid #eee;"> | <img src="./assets/image02.png" width="250" style="border-radius: 10px; border: 2px solid #eee;"> | <img src="./assets/image03.png" width="250" style="border-radius: 10px; border: 2px solid #eee;"> |

---

## 🛠️ Technical Engineering Features
This project implements high-level architectural patterns in React Native:

1.  **State Persistence**: Using `useState` hooks for real-time data binding between input and the task list.
2.  **Data Integrity**: Implementing **Immutability** patterns using `.map()` and `.filter()` to manage task lifecycle safely.
3.  **Performance Optimization**: Optimized rendering using the `FlatList` component for efficient memory management during scrolling.
4.  **Interactive UI**: Custom feedback loops using `TouchableOpacity` and dynamic conditional styling for completed items.

---

## 💻 Core Logic Overview
The following snippet represents the core engine of the application, managing task toggling and data removal:

```javascript
// Toggle Completion Status (Immutability Pattern)
const toggleCompleteHandler = (id) => {
  setCourseGoals(prevGoals => 
    prevGoals.map(goal => goal.id === id ? { ...goal, completed: !goal.completed } : goal)
  );
};

// Remove Task from List (Filtering Pattern)
const deleteGoalHandler = (id) => {
  setCourseGoals(prevGoals => prevGoals.filter(goal => goal.id !== id));
};
