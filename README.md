# SKILL LAB PRACTICAL HACKATHON

## Final Project README

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

## 2.2 Original Twist

---

# 3. Project Intent

## 3.1 User Journey

---

# 4. Definition of Success

## 4.1 Definition of “Usable”

## 4.2 Minimum Usable Version

## 4.3 Stretch Features

---

# 5. System Overview

## 5.1 Project Type
- [x] Electronics-based
- [ ] Mechanical
- [x] Sensor-based
- [x] App-connected
- [x] Motorized
- [ ] Sound-based
- [x] Light-based
- [x] Screen/UI-based
- [x] Fabricated structure
- [x] Game logic based
- [x] Installation
- [ ] Other

## 5.2 High-Level System Description

## 5.3 Input / Output Map
| System Part | Type | What It Does |
| --- | --- | --- |

---

# 6. System Design, Sketches and Visual Planning

## 6.1 Concept Architecture/sketch/schematic

## 6.2 Labeled Build Sketch/architecture/flow diagram/algorithm

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

## 7.3 Circuit Diagram/architecture diagram

## 7.4. Power Plan
| Question | Response |
| --- | --- |
| Power source | Li-ion battery pack |
| Voltage required | ~6–8.4V for motors, stepped down to 5V logic rail |
| Current concerns | Motor load can cause voltage drop and control instability |
| Safety concerns | Prevent over-discharge, short circuits, and loose wiring |

---

# 8. Software Planning/

## 8.1 Software Tools
| Tool / Platform | Purpose |
| --- | --- |
| MicroPython | Controller-side actuation logic |
| Python + Pygame + OpenCV | Marker tracking, game logic, projection updates |
| Fusion / Blender / Illustrator | Prototyping and visual planning |

## 8.2 Software Logic/Algorithm
- Initialize controller motor pins, PWM channels, and communication interface.
- Start laptop-side camera capture and marker tracking.
- Receive movement commands from control interface.
- Detect marker pose with OpenCV ArUco.
- Validate movement against game-space obstacles/rules.
- Send motor actions to controller and update projected visuals.
- On timeout/no command, stop motors as fail-safe.
- Reset level state after completion/restart trigger.

## 8.3 Code Flowchart

---

# 9. Bill of Materials

## 9.1 Full BOM
| Item | Quantity | In Kit? | Need to Buy? | Estimated Cost | Material / Spec | Why This Choice? |
| --- | ---: | --- | --- | ---: | --- | --- |

## 9.2 Material Justification

## 9.3 Items You chose
| Item | Why Needed | Purchase Link | Latest Safe Date to Procure | Status |
| --- | --- | --- | --- | --- |

## 9.4 Budget Summary
| Budget Item | Estimated Cost |
| --- | ---: |
| Electronics | 400 |
| Mechanical parts | 200 |
| Fabrication materials | 0 (available on campus) |
| Purchased extras | 0 |
| Contingency | 300 |
| **Total** | **900** |

## 9.5 Budget Reflection

---

# 10. Planning the Work

## 10.1 Team Working Agreement

## 10.2 Task Breakdown
| Task ID | Task | Owner | Estimated Hours | Deadline | Dependency | Status |
| --- | --- | --- | ---: | --- | --- | --- |

## 10.3 Responsibility Split
| Area | Main Owner | Support Owner |
| --- | --- | --- |

---

# 11 hour Milestones

## 11.1 8-hour Plan(tentetively you may set)

### Bi Hour 1 — Plan and De-risk
- [x] Idea finalized
- [x] Core interaction decided
- [x] Sketches made
- [x] BOM completed
- [ ] Purchase needs identified
- [ ] Key uncertainty identified
- [x] Basic feasibility tested

### Bi Hour 2 — Build Subsystems
- [x] Electronics tests completed
- [ ] CAD / structure planning completed
- [ ] App UI started if needed
- [x] Mechanical concept tested
- [x] Main subsystems partially working

### Bi Hour 3 — Integrate
- [x] Physical body built
- [x] Electronics integrated
- [x] Code connected to hardware
- [ ] App connected if required
- [x] First playable version exists

### Bi Hour 4 — Refine and Finish
- [x] Technical bugs reduced
- [x] Playtesting completed
- [x] Improvements made
- [x] Documentation completed
- [x] Final build ready

---

# 12. Update Log

## 12.2 Update Log
| Days | Planned Goal | What Actually Happened | What Changed | Next Steps |
| --- | --- | --- | --- | --- |
| Day 1 |  |  |  |  |
| Day 2 |  |  |  |  |
| Day 3 |  |  |  |  |
| Day 4 |  |  |  |  |

---

# 13. Risks and Unknowns

## 13.1 Risk Register
| Risk | Type | Likelihood | Impact | Mitigation Plan | Owner |
| --- | --- | --- | --- | --- | --- |
| Unstable Wi-Fi between laptop and controller | Technical | Medium | High | Keep close-range network, stable power, fail-safe motor stop |  |

## 13.2 Biggest Unknown Right Now

---

# 14. Testing

## 14.1 Technical Testing Plan
| What Needs Testing | How You Will Test It | Success Condition |
| --- | --- | --- |
| Wi-Fi command-to-motor response | Send movement commands and observe actuation | Both motors respond accurately and consistently |

## 14.2 Testing and Debugging Log
| Date | Problem Found | Type | What You Tried | Result | Next Action |
| --- | --- | --- | --- | --- | --- |

## 14.3 Playtesting Notes
| Tester | What They Did | What Confused Them | What They Enjoyed | What You Will Change |
| --- | --- | --- | --- | --- |

---

# 15. Build Documentation

## 15.1 Fabrication Process(if any)

---

# 16 Build Photos

---

# 17. Final Outcome

## 17.1 Final Description

## 17.2 What Works Well

## 17.3 What Still Needs Improvement

## 17.4 What Changed From the Original Plan

---

# 18. Reflection

## 18.1 Team Reflection

## 18.2 Technical Reflection

## 18.3 Design Reflection

## 18.4 If You Had One More hour

---

# 19. Final Submission Checklist

- [ ] Team details are complete
- [ ] Project description is complete
- [ ] Inspiration sources are included
- [ ] Sketches are added
- [ ] BOM is complete
- [ ] Purchase list is complete
- [ ] Budget summary is complete
- [ ] Mechanical planning is documented if applicable
- [ ] App planning is documented if applicable
- [ ] Code flowchart is added
- [ ] Task breakdown is complete
- [ ] Weekly logs are updated
- [ ] Risk register is complete
- [ ] Testing log is updated
- [ ] Playtesting notes are included
- [ ] Build photos are included
- [ ] Final reflection is written
