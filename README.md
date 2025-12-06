🚗 Braking Dynamics Simulator
This interactive simulator allows users to compare the stopping performance and safety margins of a human-driven vehicle against an autonomous (AI) system under various road conditions and driver states.
Key Features
•	Dual Mode Comparison: Switch instantly between Human Driver and Autonomous AI modes.
•	Safety Technology Intervention: Simulate the impact of modern safety features like Automatic Emergency Braking (AEB) and Emergency Brake Assist (EBA).
•	Real-time Analysis: Visual simulation, key metrics (reaction distance, braking distance, total time), and a dynamic Velocity vs. Time graph provide instant feedback on physics inputs.
Simulation Modes
Mode	Description	Key Physics
Human Driver	Simulates driver response based on user-defined Reaction Time and Deceleration. Allows modeling impairment.	User-Controlled $t_{react}$ and Deceleration
Autonomous AI	Simulates optimized braking with minimal latency (0.05s) and maximum safe deceleration, including an Optimal Coast feature to brake precisely at the required point.	System-Optimized $t_{react}$ and Deceleration
Human Driver Modifiers
Modifier	Effect	Constraints
Impaired Driver	Enforces a minimum reaction time of 2.50s and reduces the effective deceleration by 20%.	Allows customization of reaction time above the 2.50s minimum.
Modern Safety Tech	Activates AEB/EBA intervention, overriding human input only if a collision is imminent. The system applies higher deceleration ($a \times 1.3$) with minimal reaction delay ($0.1\text{s}$).	Only intervenes to prevent a predicted collision.
Core Inputs
Variable	Unit	Function
Initial Velocity (u)	$\text{km/h}$ 	The starting speed of the vehicle.
Reaction Time ($t_{react}$)	$\text{s}$ 	The time delay before brakes are applied (human input only). Range: 0.1s to 10.0s.
Deceleration ($a$)	$\text{m/s}^2$ 	The maximum braking force applied to the wheels. (Higher values simulate better tire grip/road condition).
Target Separation ($s$)	$\text{m}$ 	The initial distance to the obstacle (boy).
Stopping Distance Formula:
$$d_{total} = d_{react} + d_{brake}$$$$d_{react} = u \times t_{react}$$$$d_{brake} = \frac{u^2}{2a}$$
Where $u$ is velocity in $\text{m/s}$ and $a$ is deceleration in $\text{m/s}^2$.


