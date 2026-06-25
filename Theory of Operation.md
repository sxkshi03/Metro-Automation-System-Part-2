## Theory of Operation

### 1. Train Departure

The sequence begins when the **Start Pushbutton** is pressed. If all safety conditions are healthy and no stop conditions exist, the **Train_Running** status is energized. The train is considered to be travelling toward the next station.

### 2. Station Detection

When the train reaches the station, the **Station_Detect** sensor becomes active. This causes the **Brake_Applied** bit to latch, initiating the stopping sequence.

### 3. Train Stopping

After brake application, a timer begins counting to simulate train deceleration and alignment at the platform. Once the timer completes, the **Train_Stop** state is latched, indicating that the train has safely stopped at the station.

### 4. Door Opening Sequence

Following a short safety delay, the doors are commanded to open automatically. The **Door_Open** state is latched while the **Door_Close** state is reset.

### 5. Passenger Exchange

A boarding timer provides a dwell period during which passengers can enter and exit the train.

### 6. Door Closing Sequence

After the dwell period expires, the system checks for any door obstruction condition. If no obstacle exists, a closing warning timer runs and the doors are closed automatically.

### 7. Departure Preparation

Once the doors are confirmed closed, an additional departure delay is provided. This simulates platform clearance checks before train movement.

### 8. Brake Release and Restart

The **Train_Stop** and **Brake_Applied** states are reset. An internal memory bit is then energized to trigger the next departure cycle automatically.

### 9. Continuous Operation

The train repeatedly performs the following cycle:

**Depart → Travel → Detect Station → Stop → Open Doors → Passenger Wait → Close Doors → Release Brakes → Depart Again**

This creates a fully automated metro station servicing sequence.

---

## Safety Interlocks

* Emergency stop immediately prevents train movement.
* Signal interlock prevents departure under unsafe signal conditions.
* Track interlock prevents train movement when the route is unavailable.
* Door obstacle detection prevents door closure when an obstruction is present.
* Train movement is only permitted when brakes are released and all safety conditions are satisfied.

---

## Applications

* Metro rail automation training
* PLC sequencing practice
* Industrial automation education
* Railway signaling demonstrations
* State-machine and timer-based control studies
* Ladder Logic learning projects

---

## Tags Overview

| Tag            | Function                       |
| -------------- | ------------------------------ |
| Train_Running  | Indicates train is moving      |
| Train_Stop     | Indicates train is stationary  |
| Brake_Applied  | Simulates train braking        |
| Station_Detect | Station arrival sensor         |
| Door_Open      | Door open status               |
| Door_Close     | Door closed status             |
| Door_Obstacle  | Door obstruction input         |
| Signal         | Signal interlock               |
| Track          | Track availability interlock   |
| Emergency_Stop | Emergency stop condition       |
| Memory_1.0     | Automatic sequence restart bit |
| Timer_1        | Door opening delay             |
| Timer_2        | Passenger boarding time        |
| Timer_3        | Door closing delay             |
| Timer_4        | Train stopping timer           |
| Timer_5        | Departure preparation timer    |

---

## Project Files

### Ladder Logic Screenshots

* [Ladder Logic Part 1](./Ladder_Logic1.png)
* [Ladder Logic Part 2](./Ladder_Logic2.png)
* [Ladder Logic Part 3](./Ladder_Logic3.png)

### Demonstration Video

* [Metro Automation System Demo](./Metro_Automation_System_Part_2.mp4)

