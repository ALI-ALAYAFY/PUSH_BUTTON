# PUSH_BUTTON
Pushbuttons or switches connect two points in a circuit when you press them. I make a circuit using tinkercad, pushbutton circuit using both of Arduino uno and pushbutton and resistors.
//
The button can be used as a way for a user to control the robot: The robot can check if the button is pressed in order to "start" or "pause" its task. The robot can pause until the button is pressed before performing the next step in a task.

--CODE--


int buttonState = 0;

void setup()
{
  pinMode(2, INPUT);
  pinMode(13, OUTPUT);
}

void loop()
{
  // read the state of the pushbutton
  buttonState = digitalRead(2);
  // check if pushbutton is pressed. if it is, the
  // button state is HIGH
  if (buttonState == HIGH) {
    digitalWrite(13, HIGH);
  } else {
    digitalWrite(13, LOW);
  }
  delay(10); // Delay a little bit to improve simulation performance
}
