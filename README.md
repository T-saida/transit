# Assignment 2: Factory Method & Abstract Factory


---

## Project Overview
This Java application combines two Creational Design Patterns:
1. **Factory Method**: Manages logistics operations (`Truck` and `Ship` delivery workflows).
2. **Abstract Factory**: Creates cross-platform UI component families (`Button` and `Checkbox` for Windows and macOS).

Both pattern implementations work together without branching on concrete product classes during execution.

---

## Project Structure

```text
src/main/java/
├── app/
│   ├── DeliveryApplication.java   # Client class accepting Logistics and GUIFactory
│   └── Main.java                  # Application entry point with input validation
├── transport/
│   ├── Transport.java             # Product interface
│   ├── Truck.java                 # Concrete Product (Road)
│   ├── Ship.java                  # Concrete Product (Sea)
│   ├── Logistics.java             # Creator abstract class
│   ├── RoadLogistics.java         # Concrete Creator (Road)
│   └── SeaLogistics.java          # Concrete Creator (Sea)
└── ui/
    ├── Button.java                # Abstract Product A
    ├── Checkbox.java              # Abstract Product B
    ├── WindowsButton.java         # Concrete Product A1
    ├── MacOSButton.java           # Concrete Product A2
    ├── WindowsCheckbox.java       # Concrete Product B1
    ├── MacOSCheckbox.java         # Concrete Product B2
    ├── GUIFactory.java            # Abstract Factory interface
    ├── WindowsFactory.java        # Concrete Factory 1
    └── MacOSFactory.java          # Concrete Factory 2
