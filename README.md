# FinalProject-Cat-Toy

### Main idea: 
  An autonomous cat toy designed to simulate the behavior of a living prey that "watches" its surroundings. The system stays in a low-power "lookout" mode, using a rotating sensor to detect presence without needing to move the entire mechanical arm. Instead of just spinning aimlessly, it remains still until it senses an interaction, at which point it "comes to life" with randomized, reactive movements to keep the cat engaged and prevent the toy from becoming predictable

#### BOM:
  - [ ] Microcontroller: Arduino Uno 
  - [ ] Sensing: Ultrasonic distance sensor
  - [ ] Actuation: 3 x Micro-servos (1 for the radar scan, 2 for the 3D wand movement)
  - [ ] Power: 9V DC Source (Battery or external supply)
  - [ ] Hardware: Base Housing (Protective enclosure and mechanical wand)

#### Tutorial 
Sonar system: https://www.youtube.com/watch?v=61HriLtiiVQ

#### Q1 - What is the system boundary?
  - [ ] The system boundary is defined by the base housing, which is the physical enclosure that separates the internal electronics from the external environment.
  - [ ] Inside the boundary: The Arduino Uno board, batteries, and the internal parts of the motors.
  - [ ] Outside the boundary: The cat, the floor, and the room environment that the sensor monitors.

#### Q2 - Where does intelligence live?
  - [ ] All processing and decision-making happen locally on the Arduino Uno.

#### Q3 - What is the hardest technical problem?
  - [ ] Implementing a real-time detection logic that distinguishes a fast-moving cat from background noise, and managing the power supply to prevent the Arduino from resetting when all three servos             move simultaneously.

#### Q4 - What is the minimum demo?
  - [ ] A successful demo shows the toy in a resting state that immediately triggers the wand when an object is detected within range.

#### Q5 - Why is this not just a tutorial?
  - [ ] It involves building a custom state machine to handle behavior transitions (like moving from "waiting" to "active"), which requires more complex architectural decisions than a basic "on/off"             guide.
  - [ ] It requires custom architectural choices to manage non-blocking timing, ensuring the sensor remains active while the motors are executing complex movement patterns.
