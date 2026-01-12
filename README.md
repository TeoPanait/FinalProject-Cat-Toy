# FinalProject-Cat-Toy

### Main idea: 
  An autonomous cat toy designed to simulate the behavior of a living prey that "watches" its surroundings. The system stays in a low-power "lookout" mode, using a rotating sensor to detect presence without needing to move the entire mechanical arm. Instead of just spinning aimlessly, it remains still until it senses an interaction, at which point it "comes to life" with randomized, reactive movements to keep the cat engaged and prevent the toy from becoming predictable

#### Q1 - What is the system boundary?
  - [ ] The system boundary is defined by the base housing, which is the physical enclosure that separates the internal electronics from the external environment.
  - [ ] Inside the boundary: The Arduino Uno board, batteries, and the internal parts of the motors.
  - [ ] Outside the boundary: The cat, the floor, and the room environment that the sensor monitors.

#### Q2 - Where does intelligence live?
  - [ ] All processing and decision-making happen locally on the Arduino Uno.

#### Q3 - What is the hardest technical problem?
  - [ ] The primary technical challenge is implementing a real-time detection logic that distinguishes between slow-moving background objects and the sudden, high-speed displacement changes caused by a             cat's attack.

#### Q4 - What is the minimum demo?
  - [ ] A successful demo shows the toy in a resting state that immediately triggers the wand when an object is detected within range.

#### Q5 - Why is this not just a tutorial?
  - [ ] It involves building a custom state machine to handle behavior transitions (like moving from "waiting" to "active"), which requires more complex architectural decisions than a basic "on/off" guide.
  - [ ] It requires custom architectural choices to manage non-blocking timing, ensuring the sensor remains active while the motors are executing complex movement patterns.
