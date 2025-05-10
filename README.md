# Quamtum-Simulator
The Quantum Mechanics Explorer is an advanced, interactive web-based application designed to simulate and visualize quantum mechanics concepts, specifically tailored for a 2-qubit quantum system. Built using HTML, JavaScript, and Three.js, it provides an accessible platform for users—ranging from beginners to advanced learners—to experiment with quantum circuits, observe quantum phenomena like superposition and entanglement, and gain a deeper understanding of quantum computing principles. The application combines a user-friendly interface with rich visualizations and educational features, making it a powerful tool for learning and exploration.

Key Features
2-Qubit Quantum System:
Simulates a 2-qubit system, represented as a 4D complex vector (
∣
00
⟩
,
∣
01
⟩
,
∣
10
⟩
,
∣
11
⟩
∣00⟩,∣01⟩,∣10⟩,∣11⟩).
Supports quantum phenomena such as superposition, entanglement, and measurement-induced state collapse.
Comprehensive Quantum Gates:
Hadamard (H): Creates superposition (
∣
0
⟩
→
∣
0
⟩
+
∣
1
⟩
2
∣0⟩→ 
2
​
 
∣0⟩+∣1⟩
​
 ).
Pauli-X (X): Flips qubit states (
∣
0
⟩
→
∣
1
⟩
∣0⟩→∣1⟩).
Pauli-Z (Z): Flips the phase of 
∣
1
⟩
∣1⟩.
Rotation-Z (Rz, π/4): Applies a phase rotation for complex state manipulation.
CNOT: Entangles qubits, with Qubit 1 as control and Qubit 2 as target.
Controlled-Z (CZ): Applies a conditional phase flip, enabling phase-based entanglement.
Interactive Circuit Building:
Users select a qubit and gate via dropdown menus to dynamically construct quantum circuits.
Operations like applying gates, measuring, resetting, or undoing are intuitive and immediate.
Circuit Diagram Visualization:
An HTML5 Canvas displays a graphical quantum circuit, showing qubit wires and applied gates.
Single-qubit gates (H, X, Z, Rz) appear as labeled boxes; CNOT and CZ show control-target connections.
Updates in real-time as gates are added or undone.
Dual Bloch Sphere Visualization:
Two 3D Bloch spheres (rendered with Three.js) visualize the reduced density matrix states of both qubits.
Shows superposition and entanglement effects (entangled qubits may lack a definite Bloch vector).
Provides an intuitive representation of qubit states in 3D space.
Undo Operation:
Allows users to revert the last gate application, facilitating experimentation and error correction.
Maintains a history of operations and states for seamless undoing.
Save and Load Circuits:
Save: Exports the circuit’s gate sequence and final state as a JSON file.
Load: Imports a JSON file to restore a saved circuit and its state.
Uses Blob API and FileReader for robust file handling.
Tutorial Mode:
Guides users through creating a Bell state (
∣
00
⟩
+
∣
11
⟩
2
2
​
 
∣00⟩+∣11⟩
​
 ) in three steps: Hadamard on Qubit 1, CNOT, and measurement.
Displays instructions and pre-selects gates to simplify learning for beginners.
Hides after completion or on reset.
Educational Output:
Displays the quantum state in Dirac notation (e.g., 
0.71
∣
00
⟩
+
0.71
∣
11
⟩
0.71∣00⟩+0.71∣11⟩).
Shows probabilities for all basis states and detects entanglement, with explanatory text.
Explains operations and states in simple terms, enhancing accessibility.
Error Handling:
Prevents invalid actions, such as applying gates after measurement, with clear alerts.
Disables the "Apply Gate" button post-measurement until reset.
Alerts users when attempting to undo with no prior operations.
Technical Details
Quantum Mechanics Implementation:
Uses custom JavaScript for quantum operations, avoiding external library dependencies.
Represents the 2-qubit state as a 4D complex vector and applies gates via matrix multiplication.
Handles single-qubit gates (H, X, Z, Rz) using tensor products and two-qubit gates (CNOT, CZ) directly on the 4D state.
Measurement collapses the state based on computed probabilities, simulating quantum randomness.
Visualization:
Circuit Diagram: Drawn on an HTML5 Canvas, with qubit wires, gate boxes, and control-target lines for multi-qubit gates.
Bloch Spheres: Rendered with Three.js, showing qubit states via reduced density matrices. Each sphere includes a wireframe sphere, axes, and a state vector arrow.
Real-time updates ensure visualizations reflect the current quantum state.
State Management:
Tracks circuit history (gates and states) for undo functionality and saving/loading.
Manages measurement state to enforce quantum mechanics rules (no gates post-measurement).
Dependencies:
Three.js (loaded via CDN) for 3D Bloch sphere rendering.
No quantum computing libraries, ensuring portability and reliability.
User Experience
Getting Started:
Save the code as quantum_simulator.html and open it in a web browser (requires internet for Three.js).
The interface presents a clean layout with dropdowns for qubit and gate selection, buttons for actions, and visualizations.
Building Circuits:
Select a qubit and gate, then click "Apply Gate" to add to the circuit.
Watch the circuit diagram and Bloch spheres update instantly.
Use "Undo Last Gate" to experiment freely.
Exploring Quantum Phenomena:
Apply Hadamard and CNOT to create entangled states like Bell states.
Use CZ for phase-based entanglement or Rz for fine-tuned phase control.
Measure to observe state collapse and quantum correlations.
Learning and Saving:
Start the tutorial to learn how to create a Bell state step-by-step.
Save circuits to JSON files for later use or share with others.
Load saved circuits to resume experiments.
Visual and Textual Feedback:
The circuit diagram shows the sequence of operations.
Bloch spheres visualize qubit states in 3D.
The output panel explains the state, probabilities, and entanglement in clear language.
Example Use Case: Creating a Bell State
Select Qubit 1 and apply Hadamard (creates 
∣
0
⟩
+
∣
1
⟩
2
⊗
∣
0
⟩
2
​
 
∣0⟩+∣1⟩
​
 ⊗∣0⟩).
Apply CNOT (produces 
∣
00
⟩
+
∣
11
⟩
2
2
​
 
∣00⟩+∣11⟩
​
 ).
Observe the circuit diagram showing H and CNOT, Bloch spheres indicating entanglement, and output confirming the entangled state.
Measure to get 
∣
00
⟩
∣00⟩ or 
∣
11
⟩
∣11⟩, save the circuit, or undo to try a different gate like CZ.
Why It’s Amazing
Educational Power: Combines hands-on experimentation with clear explanations, making quantum mechanics accessible to all skill levels.
Rich Visualizations: The circuit diagram and dual Bloch spheres provide intuitive insights into quantum states and operations.
Interactivity: Features like undo, save/load, and tutorial mode encourage exploration and learning.
Versatility: Supports a wide range of quantum operations, from basic gates to complex entangled states.
Robust Design: Custom quantum mechanics implementation and error handling ensure reliability and portability.
The Quantum Mechanics Explorer is a comprehensive tool that showcases the fascinating world of quantum mechanics through interactive programming. It’s ideal for students, educators, hobbyists, and researchers looking to explore quantum computing concepts in a dynamic, visual, and educational environment.
