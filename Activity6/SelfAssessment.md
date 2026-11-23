# Activity 6: Final Self-Assessment

## Learning Outcome 1: Define EDP Components

### 1. What is an event? Give two examples.
An event is an action or occurrence detected by a program. Examples include clicking a button and pressing a keyboard key.

### 2. What is an event source? Give two examples.
An event source is the object or component that generates an event. Examples include a button and a text field.

### 3. What is an event listener? Give two examples.
An event listener is an object or registered component that waits for and receives notification of a particular event. Examples include an `ActionListener` listening for button actions and a `KeyListener` listening for keyboard events.

### 4. What is an event handler? Give two examples.
An event handler is the code that runs in response to an event. Examples include code that clears a text field when Clear is clicked and code that updates a counter when Increment is clicked.

### 5. Draw a diagram showing how these four components relate to each other.

```text
Event Source
     |
     | generates
     v
   Event
     |
     | received by
     v
Event Listener
     |
     | invokes
     v
Event Handler
     |
     v
Application response
```

## Learning Outcome 2: Compare Paradigms

### 6. How does procedural programming differ from event-driven programming?
Procedural programming follows a planned sequence of instructions. Event-driven programming waits for events and runs the relevant handlers when those events occur.

### 7. What is the main advantage of event-driven programming for GUIs?
It allows a graphical application to respond naturally to user interactions such as clicks, key presses, and selections.

### 8. In which scenario would you choose procedural programming over event-driven?
A simple task with a fixed sequence of steps, such as reading values, calculating a total, and printing the result, can be implemented procedurally.

## Learning Outcome 3: Event Loop and Queue

### 9. What is the event loop? What does it do?
The event loop repeatedly checks for pending events and dispatches them to the appropriate handlers.

### 10. What is the event queue? How does it work?
The event queue stores events that are waiting to be processed. Events are taken from the queue for dispatch and handling.

### 11. Why should the event loop never be blocked?
If a handler takes too long on the GUI event thread, other events cannot be processed promptly and the application may appear frozen.

### 12. What is the EDT in Java Swing?
The Event Dispatch Thread is the thread responsible for processing Swing GUI events and performing most Swing component updates.

## Learning Outcome 4: Real-World Examples

### 13. List five real-world event-driven systems.
1. ATM machine
2. Microwave oven
3. Traffic light system
4. Elevator
5. Smartphone touchscreen

### 14. For one system, identify all four EDP components.
For an ATM:
- Event source: Keypad button.
- Event: A keypad button is pressed.
- Listener: ATM software or keypad listener.
- Handler: Read the input and validate the PIN or menu selection.

### 15. Why are most modern applications event-driven?
Many modern applications have graphical interfaces and must respond to user actions, timers, messages, and other events. Event-driven programming helps organize those responses.

## Week 1 Summary

Event-Driven Programming (EDP) is a programming approach in which the application responds to events. An event is an occurrence such as a button click or key press. An event source generates the event, a listener receives notification of it, and an event handler performs the required action. The event queue stores events waiting to be processed, while the event loop checks the queue and dispatches events. In Java Swing, the Event Dispatch Thread (EDT) handles GUI events and Swing updates.

Procedural programming follows a predefined sequence of instructions. Event-driven programming is organized around events and handlers, making it useful for graphical user interfaces. A procedural calculator asks for input in a fixed order, while an event-driven calculator lets a user click buttons to enter values and operators.

A GUI should remain responsive. Long-running tasks should not block the EDT; they should run in a background thread, with Swing updates scheduled on the EDT. Common problems include missing listeners, blocking the EDT, updating GUI components from the wrong thread, and retaining references to components that have been removed.

Examples of event-driven systems include ATMs, microwaves, traffic lights, elevators, smartphones, video games, and online shopping websites.
