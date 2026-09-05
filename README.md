# Arduino LED Light Patterns 💡

A simple Arduino project for controlling multiple LEDs and creating
different programmable lighting patterns.

## 📌 About the Project

This project demonstrates how to control **14 LEDs** using an Arduino board.
Each LED is connected to a digital output pin, and different lighting
patterns are created by turning the LEDs ON and OFF with programmed delays.

The project includes **13 different LED patterns**, from simple sequential
lighting to more dynamic back-and-forth effects.

## 🔧 Hardware

- Arduino board
- 14 × LEDs
- 14 × current-limiting resistors
- Breadboard
- Jumper wires

After connecting the LEDs to the Arduino UNO and uploading the program, the final hardware setup looks like this:

<p align="center"> <img src="images/final-result.jpg" width="800"> </p>

The LEDs can produce different lighting sequences and effects according to the programmed patterns.

## 🔌 LED Pin Configuration

The LEDs are connected to Arduino digital pins:

| LED | Arduino Pin |
|-----|-------------|
| LED 0 | 0 |
| LED 1 | 1 |
| LED 2 | 2 |
| LED 3 | 3 |
| LED 4 | 4 |
| LED 5 | 5 |
| LED 6 | 6 |
| LED 7 | 7 |
| LED 8 | 8 |
| LED 9 | 9 |
| LED 10 | 10 |
| LED 11 | 11 |
| LED 12 | 12 |
| LED 13 | 13 |

> **Note:** Make sure each LED is connected through an appropriate
> current-limiting resistor.

## ⚙️ How It Works

### 1. Pin Setup

In the `setup()` function, all LED pins are configured as digital outputs.


pinMode(led0, OUTPUT);
pinMode(led1, OUTPUT);
pinMode(led2, OUTPUT);
// ...
pinMode(led13, OUTPUT);
2. Lighting Patterns

The project contains 13 different functions:

blink_1()
blink_2()
blink_3()
...
blink_13()

Each function represents a different lighting pattern.

The patterns control individual LEDs using:

digitalWrite(pin, HIGH);
digitalWrite(pin, LOW);

HIGH turns an LED on and LOW turns it off.

3. Timing

The speed of the effects is controlled using delay().

For example:

int t = 80;

means that the program waits approximately 80 milliseconds between
LED state changes.

Changing this value changes the animation speed.

🔄 Main Program Loop

The loop() function runs the lighting patterns sequentially:

void loop()
{
  blink_1();
  blink_1();

  blink_2();
  blink_2();

  blink_3();
  blink_3();

  // ...

  blink_13();
  blink_13();
}

Each pattern is executed twice before moving to the next pattern.

After blink_13() finishes, the Arduino starts again from blink_1().

✨ Patterns

The project contains different sequences such as:

Sequential LED activation

Sequential LED deactivation

Moving light effects

Forward and backward effects

Multiple LED combinations

Repeating light sequences

Each pattern is implemented as a separate function, making it easy to
modify or add new effects.

🛠️ Customization

You can easily change the behavior of the project by modifying:

Animation Speed

Change:

int t = 80;

For a faster effect:

int t = 30;

For a slower effect:

int t = 200;
Create a New Pattern

Add a new function:

void blink_14()
{
  digitalWrite(led0, HIGH);
  
  delay(100);

  digitalWrite(led0, LOW);
  
  delay(100);
}

Then call it from loop():

blink_14();

🚀 Uploading the Code

Connect the Arduino board to your computer.

Open the project in the Arduino IDE.

Select the correct Arduino board.

Select the correct serial port.

Click Upload.

The LED patterns will start automatically.

🏁 Final Result

After connecting the LEDs to the Arduino UNO and uploading the program, the final hardware setup looks like this:

<p align="center"> <img src="images/final-result.jpg" width="800"> </p>

The LEDs can produce different lighting sequences and effects according to the programmed patterns.

📂 Project Structure
Arduino-LED-Patterns/
│
├── LED_Patterns.ino
└── README.md

🎯 Purpose

This project is intended as a simple example of:
Arduino digital output control
LED sequencing
Timing with delay()
Creating programmable lighting effects
Organizing multiple Arduino animations into functions
