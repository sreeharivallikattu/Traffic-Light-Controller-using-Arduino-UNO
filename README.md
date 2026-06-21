# Traffic Light Controller using Arduino UNO

## Overview

This project implements a Smart Traffic Light Controller using Arduino UNO. The system controls traffic flow using a finite state machine architecture and non-blocking timing logic based on the `millis()` function.

The controller cycles through RED, GREEN, and YELLOW traffic states while also supporting a pedestrian crossing request button.

Unlike traditional delay-based implementations, this project uses event-driven and non-blocking embedded programming techniques similar to real traffic control systems.

## Features

* Automatic traffic light sequencing
* Pedestrian crossing request button
* Non-blocking timing using `millis()`
* Finite State Machine (FSM) implementation
* Event-driven embedded logic
* Modular and scalable code structure

## Hardware Components

* Arduino UNO
* Red LED
* Yellow LED
* Green LED
* Push Button
* Breadboard
* Jumper Wires
* 220Ω Resistors

## Circuit Connections

| Component    | Arduino Pin |
| ------------ | ----------- |
| Red LED      | D8          |
| Yellow LED   | D9          |
| Green LED    | D10         |
| Push Button  | D7          |
| LED Cathodes | GND         |

## Working Principle

The traffic controller operates using three states:

* RED
* GREEN
* YELLOW

Each state remains active for a predefined duration:

| State  | Duration  |
| ------ | --------- |
| RED    | 5 seconds |
| GREEN  | 5 seconds |
| YELLOW | 2 seconds |

The system uses the `millis()` function to track elapsed time without blocking program execution.

### Pedestrian Crossing Logic

A pedestrian can request crossing using a push button.

When the button is pressed during the GREEN state:

* The controller waits for a minimum green duration
* The system transitions early to YELLOW
* The traffic light then switches to RED

This demonstrates event-driven control logic used in real embedded systems.

## State Diagram

RED → GREEN → YELLOW → RED

Pedestrian requests can shorten the GREEN duration safely.

## Concepts Demonstrated

* Finite State Machines (FSM)
* Non-blocking Programming
* Embedded Timing Systems
* Event-driven Logic
* GPIO Control
* Edge Detection
* Traffic Control Logic

## Applications

* Smart Traffic Systems
* Embedded Controllers
* Event-driven Embedded Systems
* Real-time Control Systems

## Future Improvements

* LCD Display Integration
* Countdown Timer Display
* Multiple Traffic Junctions
* Emergency Vehicle Override
* Buzzer for Pedestrian Crossing
* IoT-based Traffic Monitoring

## Results

The project successfully demonstrates a fully functional smart traffic controller capable of handling timed traffic sequencing and pedestrian crossing requests using non-blocking embedded programming techniques.

## Author

**Sreehari Vallikattu**

Electrical and Electronics Engineering Student

