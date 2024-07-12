# Event Handling
## What is event
It is an action or occurrence recognized by software, typically originating from the user's interaction with the system. They change the state in the system.

Two types of events:
- User Generated
	- Mouse
	- Keyboard
	- Action
- System Generated
	- Window
	- Focus
	- Component

## Event Handling
- **Event Source:** the object that generated the event (like a button getting clicked)
- **Event object:** An instance of `ActionEvent` Is created when the button is clicked, containing information about the click event
- **Event Listener:** The class `SimpleEventListener`  implements `ActionListner` and therefore acts as the listener
- **Event Handling Method:** The `actionPerformed` method is invoked wehn the button is clicked, and performs the required operation.