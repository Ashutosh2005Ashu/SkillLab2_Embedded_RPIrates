# SKILL LAB PRACTICAL HACKATHON

## Code Documentation (Covered Sections Only)

---

# 1. Team Identity

## 1.1 Studio / Group Name
`Project^2`

## 1.2 Team Members
| Name | Primary Role | Secondary Role | Strengths |
| --- | --- | --- | --- |
| Mrugendra Vasmatkar | Electronics / Coding / App | Documentation | Documentation, communication |
| Jyoti Bagate | Electronics / Fabrication | Coding | Material handling, hardware |

## 1.3 Project Title
`Project Project`

## 1.4 One-Line Pitch
A projected, customizable time-portal experience where engineering education is delivered through a PUBG-style battlefield format at home.

## 1.5 Expanded Project Idea
The project creates an immersive engineering-learning experience using projection, gameplay, and physical interaction. Learners solve mission-style challenges based on real engineering concepts instead of only studying theory.

Core technologies include a Raspberry Pi/ESP-class controller setup, motor control, camera tracking (OpenCV + ArUco), projected game environment, and Python-based game/control logic.

---

# 2. Inspiration

## 2.1 References
| Source Type | Title / Link | What Inspired the Project |
| --- | --- | --- |
| Video | https://www.instagram.com/reel/DW4CT7WCDry/?igsh=cXg3dzAxYmdncDBo | Projection mapping for interactive digital + physical experiences |

---

# 5. System Overview

## 5.1 Project Type
- Electronics-based
- Sensor-based
- App-connected
- Motorized
- Light-based
- Screen/UI-based
- Fabricated structure
- Game-logic based
- Installation

---

# 6. System Design

## 6.3 Approximate Dimensions
| Dimension | Value |
| --- | --- |
| Length | 16 cm |
| Width | 16 cm |
| Height | 8 cm |
| Estimated weight | 400 g |

---

# 7. Electronics Planning

## 7.1 Electronics Used
| Component | Quantity | Purpose |
| --- | ---: | --- |
| Raspberry Pi / controller board | 1 | Main controller |
| L298N Motor Driver | 1 | Motor control |
| BO Motors | 2 | Wheel rotation |
| Buck Converter | 1 | Regulated supply |
| Li-ion Battery Pack | 2 | Power |
| Projector | 1 | Display game obstacles |
| Camera (Webcam / Phone) | 1 | Marker-based position tracking |

## 7.2 Wiring Plan
Controller GPIO pins connect to L298N direction inputs, with PWM pins driving ENA/ENB for speed control. Motors connect to driver outputs.  
Battery powers the motor driver directly, and a buck converter provides regulated 5V to the controller logic side.  
All modules share common ground. Projector and camera connect to the laptop for tracking and game rendering.

## 7.4 Power Plan
| Question | Response |
| --- | --- |
| Power source | Li-ion battery pack |
| Voltage required | ~6–8.4V for motors, stepped down to 5V logic rail |
| Current concerns | Motor load can cause voltage drop and control instability |
| Safety concerns | Prevent over-discharge, short circuits, and loose wiring |

---

# 8. Software Planning

## 8.1 Software Tools
| Tool / Platform | Purpose |
| --- | --- |
| MicroPython | Controller-side actuation logic |
| Python + Pygame + OpenCV | Marker tracking, game logic, projection updates |
| Fusion / Blender / Illustrator | Prototyping and visual planning |

## 8.2 Software Logic / Algorithm
- Initialize controller motor pins, PWM channels, and communication interface.
- Start laptop-side camera capture and marker tracking.
- Receive movement commands from control interface.
- Detect marker pose with OpenCV ArUco.
- Validate movement against game-space obstacles/rules.
- Send motor actions to controller and update projected visuals.
- On timeout/no command, stop motors as fail-safe.
- Reset level state after completion/restart trigger.

---

# 9. Bill of Materials

## 9.1 Budget Summary
| Budget Item | Estimated Cost |
| --- | ---: |
| Electronics | 400 |
| Mechanical parts | 200 |
| Fabrication materials | 0 (available on campus) |
| Purchased extras | 0 |
| Contingency | 300 |
| **Total** | **900** |

---

# 11. Milestones (Completed Status Snapshot)

- Idea finalized
- Core interaction decided
- Sketches prepared
- BOM completed
- Basic feasibility tested
- Electronics tests completed
- Mechanical concept tested
- Physical + electronics integration completed
- First playable version achieved
- Playtesting and refinements completed

---

# 13. Risks and Unknowns

## 13.1 Risk Register (Known)
| Risk | Type | Likelihood | Impact | Mitigation |
| --- | --- | --- | --- | --- |
| Unstable Wi-Fi between laptop and controller | Technical | Medium | High | Keep close-range network, stable power, fail-safe motor stop |

---

# 14. Testing

## 14.1 Technical Testing Plan (Covered)
| What Needs Testing | How It Is Tested | Success Condition |
| --- | --- | --- |
| Wi-Fi command-to-motor response | Send movement commands and observe actuation | Both motors respond accurately and consistently |
