# CPNT262

## Activity Name
- Mini Activity 4 - Framework Reactivity

## Author
- Hendrich Buhrer

## Component 1: Navigation Bar

### Description:
This component represents a navigation bar with a dark mode toggle button.

### Features:
- Data binding: The navigation bar class is dynamically bound based on the darkMode variable.
- Conditional Example: It conditionally renders different SVG icons based on darkMode.
- Slots: It accepts one slot for the logo.
- Events: Clicking on the toggle button triggers the toggleDarkMode function and emits a custom event when dark mode is toggled.
- Reactivity: The darkMode variable is created using ref() to make it reactive.

## Component 2: Status Display

### Description:
This component displays a word dynamically with a rotating effect (Goes through a list of pre-selected words).

### Features:
- Data binding: The status variable is bound to the text content.
- Double mustache variable rendering: It renders the status variable.
- Props and Slots: It utilizes one slot for rendering dynamic content.
- Reactivity: Reactive variables are used for statuses, currentIndex, and status.
