# Hierarchical Menu System for Console Applications

This project provides a reusable component for creating and managing hierarchical menus in .NET console applications, implemented using two approaches: **Interfaces** and **Delegates**. The solution is divided into three projects to demonstrate the functionality.

## Project Structure

### 1. **Ex04.Menus.Interfaces**
- Implements the menu system using **interfaces**.
- Demonstrates how to define and use interfaces for hierarchical menu navigation and actions.

### 2. **Ex04.Menus.Events**
- Implements the menu system using **delegates** and **events**.
- Demonstrates the use of `Action<T>` for dynamic binding of functionality to menu items.

### 3. **Ex04.Menus.Test**
- A test application that demonstrates the usage of both menu systems.
- Contains two hierarchical menus with two levels each:
  - **Menu 1 (Interfaces-based)**:
    - `Version and Capitals`:
      - **Show Version**: Displays `App Version: 24.2.4.9504`.
      - **Count Capitals**: Prompts the user to input a sentence and counts uppercase letters.
    - `Show Date/Time`:
      - **Show Time**: Displays the current time.
      - **Show Date**: Displays today's date.
  - **Menu 2 (Delegates-based)**:
    - Identical structure and functionality to Menu 1.

---

## Features

- **Polymorphism**: Implements an extensible object-oriented design for menu management.
- **Interfaces**: Abstracts menu item behaviors for flexible implementation.
- **Delegates and Events**: Uses `Action<T>` to dynamically bind actions to menu items.
- **Collections**: Utilizes collections for dynamic management of menu items and submenus.
- **Reusable**: Designed to be integrated into other console applications.

---

## How It Works

1. **Menu Creation**:
   - Developers can define hierarchical menus by adding `MenuItem` objects to a `MainMenu` instance.
   - Submenus can be created recursively by adding `MenuItem` collections.

2. **User Interaction**:
   - The `Show()` method of `MainMenu` runs the main loop, displaying menu options and handling user input.
   - Users can navigate between levels, trigger actions, or exit the application.

3. **Customization**:
   - Action binding via interfaces or delegates allows custom actions to be executed for each menu item.
