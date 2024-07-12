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
- **Event Listener:** The class `SimpleEventListener` implements `ActionListner` and therefore acts as the listener
- **Event Handling Method:** The `actionPerformed` method is invoked when the button is clicked, and performs the required operation.


### Voting Eligibility AWT

```Java
import java.awt.*;
import java.awt.event.*;

public class VotingEligibility extends Frame implements ActionListener {
    private Label label;
    private TextField textField;
    private Button submitButton;

    public VotingEligibility() {
        label = new Label("Enter your age: ");
        textField = new TextField(3);
        submitButton = new Button("Submit");

        setLayout(new FlowLayout());
        add(label);
        add(textField);
        add(submitButton);

        submitButton.addActionListener(this);

        setTitle("Voting Eligibility Checker");
        setSize(300, 300);
        setVisible(true);

        addWindowListener(new WindowAdapter() {
            public void windowClosing(WindowEvent we) {
                System.exit(0);
            }
        });
    }

    public void actionPerformed(ActionEvent ae) {
        try {
            int age = Integer.parseInt(textField.getText());
            if (age > 18) {
                showMessage("OK");
            } else {
                showMessage("Not OK");
            }
        } catch (NumberFormatException e) {
            showMessage("Invalid input");
        }
    }

    private void showMessage(String message) {
        Dialog dialog = new Dialog(this, "Message", true);
        dialog.setLayout(new FlowLayout());
        dialog.add(new Label(message));
        Button ok = new Button("OK");
        ok.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                dialog.setVisible(false);
                dialog.dispose();
            }
        });
        dialog.add(ok);
        dialog.setSize(200, 100);
        dialog.setVisible(true);
    }

    public static void main(String[] args) {
        VotingEligibility app = new VotingEligibility();
    }
}

```

# Applet
It is a type of java program that is designed to be embedded within a web page and run in a web browser. It's a java application which extends the java.applet.Applet class or implements the javax.swing.JApplet class.
Applets often create GUIs using cmponents such as TextFields, buttons, and images to make it more interctable for the end user.
They are event driven applications such as mouse clicks, keyboard inputs and network requests.

## Life Cycle of Applet
It is the sequence of events that occur from the initialization to teh termination od an applet. 