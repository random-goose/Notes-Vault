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


### Voting Eligibility AWT

```Java
import java.awt.*;
import java.awt.event.*;

public class VotingELigibility extends Frame implements ActionListenet {
	private Label labe;
	private TextField textField;
	private Button submitButton;
	
	public votingEligibility() {
		label = new Label("Enter your age: ");
		textField = new TextField(3);
		submitButton = new Button("Submit");

		setLayout(new FlowLayout());
		add(label);
		add(textField);
		add(submitButton);

		setTitle("Voting ELigibility Checker");
		setSize(300,300);
		setVisibility(true);

		addWindowListener(new WindowAdapter()) {
			public void windowClosing(WindowEvent we) {
				System.exit(0);
			}
		}
	}

	public void actionPerformed(ActionEvent ae) {
		try{
			int age = Integer.ParseInt(textField.getText());
			if (age>18) {
				showMessage("ok");
			}
			else {
				showMessage("not");
			}
		} catch (NumberFormatException e) {
			
		}
		
	}
}
```