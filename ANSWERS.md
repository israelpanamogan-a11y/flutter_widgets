1. What is the difference between a StatelessWidget and a StatefulWidget? Give one example of each from this lab.

- A StatelessWidget is immutable. Just like in Activity 1, details such as the Name, Course, Email, and Phone Number do not change once the widget is built. A StatefulWidget is mutable. A great example of this is Activity 5, where switching between Dark Mode and Light Mode updates the UI even after the widget has been built.

2. Why is a StatefulWidget written as two classes? What does each class do?

- A StatefulWidget is split into two classes because widgets are immutable, but state is mutable. The Widget class stores fixed, immutable data and configuration settings. It cannot store or update variables that change over time. The State class, on the other hand, holds mutable data and handles user interactions, accepts, updates, and renders changes while the app is running.

3. In Activity 2, what happened when you changed \_glasses outside setState()? Why?

- Modifying \_glasses++ outside setState() updates the variable's value internally, but it fails to update the display. Without setState(), Flutter is not notified to execute the build() method, so the user interface remains unchanged despite the variable being incremented

4. Looking at the Debug Console in Activity 2, when is build() called?

- When the widget is first created. When WaterTrackerPage is loaded on the screen for the first time, Flutter executes build() to construct and display the initial UI (the 0/6 glasses.)

5. Explain the main axis and the cross axis of a Row and of a Column.

- In a Row, the main axis is horizontal (left to right) and the cross axis is vertical (top to bottom). In a Column, the main axis is vertical (top to bottom) and the cross axis is horizontal (left to right).

6. In Activity 3, what happened when you removed Expanded from a StatBox? What does Expanded do?

- When I remove Expanded from a StatBox, Flutter no longer forces the box to share the horizontal space equally with the other boxes.

7. Why do we use GridView.builder for the menu instead of a Column with many children?

- GridView.builder is used because it automatically arranges items into a 2D grid with built-in scrolling and only renders the items visible on screen to save memory

8. How do Stack and Positioned create the Best seller badge in Activity 4?

- Stack layers the badge on top of the card, and Positioned places it in the top-left corner.

9. What is the difference between customizing with ThemeData and with a style on one widget? Give one example of each from Activity 5.

- ThemeData applies styling globally across all widgets in the app (e.g., elevatedButtonTheme), whereas a widget-level style appliesonly to a single specific widget instance (e.g., setting backgroundColor on a CircleAvatar).

10. When you flip the dark-mode switch in Activity 5, which widget holds the state, and how does the change reach MaterialApp?

- ThemeDemoApp holds the \_isDark state, and when the switch is flipped, it triggers \_setDark() which calls setState() to rebuild ThemeDemoApp and pass the updated ThemeMode to the MaterialApp.
