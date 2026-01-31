# GHOST-DRIVE
Predictive obstacle avoidance using LiDAR
 Project Ghost-Drive: Virtual LiDAR Navigation
"Navigating the unseen through data, not sight."
This project simulates an autonomous robotic system that navigates a hazardous environment using Distance-Stream Processing. By utilizing Python in a Google Colab environment, we simulate a LiDAR (Light Detection and Ranging) sensor to detect obstacles and execute real-time evasive maneuvers.
📖 Project Overview
In many real-world scenarios (deep sea, thick fog, or space), cameras are useless. Robots must rely on "Time-of-Flight" sensors like LiDAR or Ultrasonic pulses. Ghost-Drive is a Python-based AI that processes raw distance data to build a spatial map and navigate safely without a single pixel of video.
🛠️ Tech Stack
 * Language: Python 3
 * Environment: Google Colab / Jupyter Notebook
 * Libraries: * NumPy: For high-speed sensor data processing.
   * Matplotlib: To visualize the robot's "Radar" view.
   * Time/Random: To simulate real-time environmental changes.
⚙️ How It Works (The Logic)
The robot operates on a Finite State Machine (FSM). It constantly asks one question: "How much space is in front of me?"
| Sensor Reading | Robot Action | Logic State |
|---|---|---|
| > 100cm | Full Acceleration | CRUISE |
| 50cm - 100cm | Reduce Speed | CAUTION |
| < 50cm | Stop & Rotate 90° | EVADE |
🚀 Key Features
 * Virtual LiDAR HUD: A live-updating plot in Google Colab that shows a "sonar-style" radar map.
 * Zero-Hardware Requirement: Uses mathematical simulations to mimic real-world physics.
 * Crash-Proof Algorithm: Uses threshold-triggered logic to ensure the robot never hits a virtual wall.
 * Maze-Solving Potential: Includes logic for the "Left-Hand Rule" to navigate through simulated corridors.
📂 Project Structure
 * Data Generation: Simulating a stream of distance numbers (integers).
 * The Processor: A Python loop that analyzes the numbers for "danger zones."
 * The Actuator: A print-based output that mimics motor commands (e.g., Motor::Forward, Motor::Turn_Left).
 * The Visualizer: A 2D Polar Plot showing where obstacles are located.
🏁 Conclusion
Ghost-Drive demonstrates that the heart of robotics isn't the hardware—it's the feedback loop. By processing simple numerical arrays, we can create complex, "intelligent" behavior that allows a machine to survive in a challenging environment.

