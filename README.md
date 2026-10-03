# Tendon-Driven Soft Robotic Gripper

**Three-finger soft robotic gripper with antagonistic tendon actuation, silicone molding, suction-assisted grasping and pressure sensing**

Academic soft-robotics project focused on the design, fabrication and experimental validation of a compliant gripper capable of adapting to rigid, irregular, deformable and wet objects.

> **Status:** Completed academic team project  
> **Team size:** 6  
> **Main areas:** Soft robotics, mechanical design, silicone molding, tendon actuation, pressure sensing, prototyping and experimental validation

---

## At a Glance

| | |
|---|---|
| **Architecture** | Three soft silicone fingers arranged radially |
| **Actuation** | Six antagonistic tendons driven through a coaxial double-spool mechanism |
| **Control complexity** | One rotational input coordinates all three fingers |
| **Finger behaviour** | Active bidirectional bending |
| **Additional adhesion** | Palm-mounted silicone suction cup |
| **Sensing** | Suction-line pressure sensing |
| **Fabrication** | FDM-printed molds/frame + cast silicone fingers |
| **Materials** | Ecoflex 00-35 FAST and Dragon Skin 10 |
| **Testing** | Grasping, coordination, suction assistance and submerged-object retrieval |

---

# Project Overview

The objective was to develop a **three-finger soft robotic gripper** capable of secure and adaptive grasping across different object geometries and environmental conditions.

The design combined several complementary mechanisms:

```text
Soft Silicone Fingers
        +
Antagonistic Tendons
        +
Coaxial Double-Spool
        +
Palm Suction Cup
        +
Pressure Sensing
```

The resulting prototype was designed to support:

- external enveloping grasps
- internal expanding grasps
- irregular-object grasping
- deformable-object handling
- misaligned approaches
- suction-assisted holding
- wet and submerged object manipulation

![Final gripper CAD](media/prototype/final%20gripper%20cad.png)

[▶ View final gripper actuation](<media/prototype/final gripper actuation video.mp4>)

---

# My Contributions

This was a **six-person academic team project**.

My main contributions were:

### Concept & Prototyping

- contributed to the overall gripper concept and manipulation approach
- participated in iterative physical prototyping
- assisted with 3D printing of several prototype components
- contributed to final mechanical assembly

### Mold Preparation & Soft Fabrication

I took primary responsibility for the **mold-preparation stage**, including:

- preparing the molds before casting
- inserting cable guides / routing features
- applying mold-release treatment
- supporting the silicone casting process
- tendon/cable insertion after fabrication

### Pressure-Sensing System

I took primary responsibility for the **pressure-sensing subsystem**, from integration through working prototype testing.

The sensor was used to provide information about suction pressure and seal quality.

The implemented prototype used this as sensing/monitoring information.

A proposed future extension is to use the pressure signal in closed-loop control:

```text
Suction Pressure
      ↓
Detect Loss of Seal
      ↓
Increase Finger Grasp
      ↓
Reduce Risk of Object Drop
```

This automatic feedback behaviour was a **future-control concept**, not part of the final implemented controller.

### Experimental Validation

I participated with the team in the full experimental testing programme, including:

- finger motion testing
- three-finger coordination
- adaptive grasping
- suction-assisted grasping
- irregular and deformable object tests
- wet/submerged-object tests

---

# Mechanical Architecture

The gripper uses **three soft silicone fingers positioned approximately 120° apart**.

Each finger is designed for compliant bending and object adaptation.

The main mechanical elements are:

```text
Rigid 3D-Printed Frame
        │
        ├── Soft Finger ×3
        │     ├── Tendon A
        │     └── Tendon B
        │
        ├── Coaxial Double Spool
        │
        ├── Servo Actuation
        │
        └── Palm Suction Cup
              │
              └── Pressure Sensor
```

The soft fingers provide compliant contact, while the tendon mechanism provides active bending in both directions.

---

# Antagonistic Tendon Actuation

Each finger contains two antagonistic tendons.

The concept is analogous to opposing biological muscle groups:

```text
Tendon A pulls
     ↓
Finger bends in one direction

Tendon B pulls
     ↓
Finger bends in the opposite direction
```

A coaxial double-spool mechanism winds one tendon set while releasing the opposing set.

This allows:

- active flexion
- active extension
- coordinated finger motion
- low actuator count
- mechanical underactuation

One rotational input controls all six tendons and coordinates the three fingers.

[▶ View final gripper actuation](<media/prototype/final gripper actuation video.mp4>)

---

# Soft Finger Design

The finger geometry was designed to support large deformation while maintaining sufficient structural stability.

Important design features included:

- tapered finger geometry
- segmented finger structure
- bidirectional bending
- compliant silicone body
- rigid mounting at the finger base
- textured contact surfaces

The finger design also incorporated **hexagonal surface microstructures** inspired by biological wet-adhesion systems.

These textures were intended to help channel fluid away from the contact region and improve grip under wet conditions.

---

# Silicone Material Strategy

Two silicone materials were combined during fabrication.

### Ecoflex 00-35 FAST

Used for greater compliance and deformation.

### Dragon Skin 10

Used to provide additional structural support and shape stability.

The fabrication approach combined both materials to balance:

```text
Compliance
    ↕
Structural Stability
```

---

# Mold-Based Fabrication

The fingers were produced using custom 3D-printed molds.

The fabrication process included:

```text
CAD Mold Design
      ↓
3D Printing
      ↓
Cable-Guide Preparation
      ↓
Mold Release
      ↓
Silicone Mixing
      ↓
Separate Casting
      ↓
Partial Curing
      ↓
Mold Combination
      ↓
Final Curing
      ↓
Demolding
      ↓
Flash Removal
      ↓
Tendon Insertion
```

## Mold Preparation

![Mold preparation](<media/fabrication/preparation of mold with cables and spray.jpg>)

Cable guides were inserted to constrain tendon routing and reduce friction before the silicone was cast.

## Silicone Mixing

![Silicone mixing](<media/fabrication/Mixing two-component silicone.jpg>)

## Two-Material Casting

![Ecoflex and Dragon Skin casting](<media/fabrication/Casting the two molds separately - Ecoflex then Dragon Skin.jpg>)

## Final Curing

![Molds overlapping for final curing](<media/fabrication/Molds overlapping and final curing.jpg>)

## Demolded Finger

![Demolded soft finger](<media/fabrication/Entire finger demolded.jpg>)

---

# Palm Suction System

A compliant silicone suction cup was integrated into the palm to complement the finger grasp.

The two mechanisms serve different roles:

```text
Soft Fingers
    ↓
Distributed Contact
+
Shear Stability

Suction Cup
    ↓
Normal Adhesion
```

When a suitable seal is formed, the suction cup provides additional resistance to pull-off forces.

![Suction cup](<media/fabrication/Suction Cup.jpg>)

![Cast suction cup](<media/fabrication/Suction Cup Cast.jpg>)

[▶ View suction-cup mold / fabrication concept](<media/fabrication/Suction Cup Casting exploded view.mp4>)

---

# Pressure Sensing

The suction line includes a pressure sensor.

The implemented sensing system provided information about the pressure level and therefore the quality of the suction seal.

This is particularly useful because suction performance depends strongly on:

- object geometry
- surface roughness
- contact alignment
- leakage
- seal quality

The pressure sensing worked on the physical prototype.

The current system uses the reading primarily as information.

A future closed-loop version could use pressure loss as a control trigger:

```text
Pressure Drop
     ↓
Possible Seal Loss
     ↓
Command Stronger Finger Closure
     ↓
Maintain Object Stability
```

That automatic response was **not implemented in the final prototype**.

---

# CAD & Mechanical Design

The repository includes both native SolidWorks files and a STEP export.

```text
cad/
├── solidworks/
│   ├── base.SLDPRT
│   ├── mold_fingers_fill_patt_v3_noBump.SLDPRT
│   ├── mold_fingers_fill_patt_v3_noBump_FINGER.SLDPRT
│   ├── molds_preview.SLDASM
│   └── soft_project_assembly.SLDASM
│
└── step/
    └── AssemblySoft.step
```

The STEP model provides a more software-independent representation of the mechanical assembly.

## Final CAD

![Final gripper CAD](media/prototype/final%20gripper%20cad.png)

## Frame / Internal Layout

![Translucent frame view](media/prototype/translucent%20view%20of%20the%20frame.png)

[▶ View exploded assembly animation](<media/prototype/final gripper exploded view.mp4>)

---

# Experimental Validation

Testing focused on verifying the gripper's key functional behaviours.

---

## 1. Bidirectional Finger Motion

The antagonistic tendons were tested for:

- flexion
- extension
- return toward neutral
- repeatability under repeated commands

The mechanism successfully demonstrated active bidirectional bending.

---

## 2. Three-Finger Coordination

The double-spool transmission was tested to verify whether all three fingers moved together under a single rotational input.

Evaluation focused on:

- simultaneous motion onset
- consistent opening/closing direction
- final finger curvature
- inter-finger timing differences

The prototype achieved coordinated three-finger motion.

Minor asymmetry was observed due to tendon friction and pretension differences.

---

# Adaptive Grasping Tests

Several grasp configurations were tested.

## External Enveloping Grasp

[▶ External enveloping grasp](<media/testing/EXTERNAL ENVELOPING GRASP.mp4>)

## Internal Expanding Grasp

[▶ Internal expanding grasp](<media/testing/INTERNAL EXPANDING GRASP.mp4>)

## Deformable / Flexible Object

[▶ Deformable-object test](<media/testing/DEFORMABLE-FLEXIBLE OBJECT.mp4>)

## Irregular Object

[▶ Irregular-object test](<media/testing/IRREGULAR OBJECT.mp4>)

## Misaligned Approach

[▶ Misaligned grasp approach](<media/testing/MISALIGNED APPROACH.mp4>)

These experiments demonstrated how compliance allows the fingers to adapt to shape and alignment variation without requiring exact geometric contact planning.

---

# Suction-Assisted Grasping

The palm suction cup was evaluated as an auxiliary adhesion mechanism.

[▶ Suction-assisted grasping](<media/testing/Suction-Assisted Grasping.mp4>)

The tests showed that suction can complement the soft fingers when an adequate seal is available.

The fingers contribute distributed contact and lateral stability, while suction contributes additional normal adhesion.

---

# Wet / Submerged Testing

Wet manipulation was an important target scenario because the finger texture and suction concept were inspired partly by biological attachment mechanisms.

## Single Object Retrieval

[▶ Single submerged-object retrieval](<media/testing/Single submerged object retrieval.mp4>)

## Multiple Object Retrieval

[▶ Multiple submerged-object retrieval](<media/testing/Multiple submerged object retrieval.mp4>)

The prototype was able to perform submerged grasping demonstrations using the compliant fingers and textured contact surfaces.

---

# Validation Against Design Objectives

| Objective | Outcome |
|---|---|
| Active bidirectional bending | ✅ Achieved |
| One-input three-finger coordination | ✅ Achieved |
| Adaptive grasping across different geometries | ✅ Achieved |
| Suction-assisted holding | ✅ Achieved |
| Physical silicone-finger fabrication | ✅ Achieved |
| Wet/submerged grasp demonstrations | ✅ Demonstrated |
| Working pressure sensing | ✅ Implemented |
| Automatic pressure-based grasp tightening | ❌ Future work |
| Quantitative grasp-force validation | ❌ Not performed |
| Closed-loop autonomous suction control | ❌ Not implemented |

The project therefore demonstrated the proposed low-complexity hybrid grasping architecture while also identifying clear areas for further development.

---

# Limitations

The prototype exhibited several expected limitations of tendon-driven soft systems.

### Tendon Transmission Variability

Cable friction, slack and pretension differences can create:

- small delays
- asymmetric finger motion
- different final curvatures

### Fabrication Variability

Manual silicone fabrication can introduce:

- bubbles
- mold tolerances
- material inconsistencies
- bending asymmetry

### Suction Seal Dependence

Suction performance depends strongly on contact geometry and seal quality.

### Primarily Qualitative Validation

Testing demonstrated functional success, but the project did not include a full quantitative benchmark of:

- grasp force
- payload capacity
- pull-off force
- bending angle
- success rate
- cycle durability

---

# Future Work

The clearest next steps are:

### Closed-Loop Pressure Feedback

Use the existing pressure sensing as feedback for automatic grasp adaptation:

```text
Pressure falls
    ↓
Detect reduced suction
    ↓
Increase finger tension
    ↓
Maintain grasp
```

### Automatic Vacuum Generation

Replace the manually driven suction source with a compact controllable pump.

### Improved Tendon Routing

Add:

- lower-friction guides
- adjustable tensioners
- better cable anchoring

### More Repeatable Silicone Fabrication

Potential improvements include:

- improved mold tolerances
- vacuum degassing
- standardized curing
- more repeatable material dosing

### Quantitative Testing

Future experiments should measure:

- bending angle
- grasp force
- payload
- suction pull-off force
- grasp success rate
- repeatability
- durability over repeated cycles

---

# Repository Structure

```text
tendon-driven-soft-gripper/
│
├── README.md
│
├── cad/
│   ├── solidworks/
│   └── step/
│
├── docs/
│   └── presentation/
│
└── media/
    ├── fabrication/
    ├── prototype/
    └── testing/
```

---

# Project Presentation

The final team presentation is included here:

```text
docs/presentation/Group 2 - Soft Robotics Project Submission-compressed.pdf
```

It contains the complete project development process, design rationale, manufacturing workflow and testing programme.

---

# Skills Demonstrated

This project provides evidence of experience in:

- soft robotics
- mechanical prototyping
- tendon-driven actuation
- compliant mechanisms
- underactuated robotic systems
- SolidWorks
- CAD
- FDM 3D printing
- mold design
- silicone casting
- Ecoflex
- Dragon Skin
- tendon routing
- mechanical assembly
- pressure sensing
- suction systems
- sensor integration
- experimental testing
- wet-environment manipulation
- robotic grasping
- design iteration
- hardware integration

---

# Team Work & Attribution

This repository represents a **six-person academic team project**.

The complete system, CAD, prototype and validation programme were developed collaboratively.

The **My Contributions** section above identifies the areas in which I had direct responsibility or significant hands-on involvement.

In particular, I took primary responsibility for:

- mold preparation
- tendon/cable insertion support
- pressure-sensor integration and testing

and contributed to:

- project concept development
- physical prototyping
- 3D printing
- assembly
- experimental validation

Electronics and actuator-control development were primarily handled by other team members, with limited input from me.

---

# Project Status

✅ **Completed academic soft-robotics project**

The physical prototype was fabricated and successfully demonstrated:

- active bidirectional finger motion
- coordinated three-finger actuation
- adaptive grasping
- suction-assisted holding
- pressure sensing
- wet/submerged object retrieval

The next development stage would focus on **closed-loop sensing and control, improved fabrication repeatability and quantitative performance evaluation**.
