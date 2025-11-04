RC Aircraft

Preliminary Report

PROJECT X 2.0
Indian Institute of Technology Mandi

ABSTRACT
This project presents the conceptualization, design, and construction of a radio-controlled (RC) fixed-wing aircraft developed for the Techfest IIT Bombay Aeromodelling Competition 2025. The aircraft is designed to achieve optimal performance in both endurance and payload-carrying missions, adhering strictly to the dimensional and performance constraints outlined in the competition rulebook. The primary objectives of the design are to maximize aerodynamic efficiency, stability, and controllability while maintaining a low structural weight and high structural integrity.

2. SUMMARY

An iterative design approach was employed, involving aerodynamic simulation(in xflr5), airfoil selection, structural optimization, and propulsion system analysis. The chosen configuration is a high-wing monoplane with inherent stability and smoother flight characteristics. A lightweight yet rigid structure is achieved using a combination of balsa wood and foam(depron) board for the wing and fuselage, respectively. The S1223 airfoil is considered for its high lift coefficient and proven low-speed performance. Power is provided by a high-efficiency brushless DC motor coupled with a matching propeller and Li-Po battery, ensuring a thrust-to-weight ratio not exceeding 1 according to competition guidelines. Control is achieved via a standard 6-channel transmitter?receiver system (FS-i6) driving servos for elevator, rudder, and aileron actuation.

The design process integrates theoretical calculations with empirical testing and computational tools to optimize wing loading, center of gravity, and propulsion efficiency. The final aircraft is expected to demonstrate excellent stability, short takeoff distance, and efficient flight performance across all mission rounds of the competition.
3. DESIGN OVERVIEW
3.1 Aircraft Configuration
The aircraft adopts a high-wing monoplane configuration. The high-wing placement lowers the center of gravity relative to the wing plane, promoting smoother flight behavior and easier recovery from disturbances ? ideal for low-speed operations.
3.2 Airfoil Selection
The airfoil determines the lift characteristics and stall performance. Based on analysis of past competition winners and aerodynamic data:

Chosen Airfoil: S1223 
Reasoning:
High maximum lift coefficient (Cl_max ? 2.0-2.2)
Gentle stall characteristics
Proven performance at low Reynolds numbers (~150,000?300,000 range for 1 m wingspan)
This ensures high lift generation even at low speeds and controlled landings.
3.3 Wing Design
Rectangular planform with rounded tips for structural simplicity and consistent lift distribution.

Wingspan: 1.0 m (as per Techfest constraint)
Chord: 0.18 m (approx.)
Aspect Ratio: ~5.5
Wing Loading: Targeted below 30 N/m? for better endurance.
Material: 3 mm balsa sheet with carbon spar reinforcement for strength.
3.4 Tail Design
Conventional tail (horizontal stabilizer + vertical fin)

Horizontal Tail Area: ~20% of wing area
Vertical Tail Area: ~10% of wing area
Purpose: Provides pitch and yaw stability, ensuring smooth response to control inputs.


3.5 Fuselage Design
Streamlined rectangular cross-section

Material: Foam board structure with balsa reinforcement
Features: Compartment for battery, receiver, ESC and golf ball carrying; detachable wing mounting for transport and repair ease.

3.6 Propulsion System

Component
Specification
Justification
Motor
1000-1200KV BLDC
High thrust-to-weight, efficient at low speeds
ESC
30A Brushless ESC
Matches motor current requirements
Battery
3S Li-Po (11.1 V, 2200 mAh)
Lightweight with adequate current capacity
Propeller
10x 4.5?
Balances thrust and endurance
Thrust/Weight Ratio
<1
Within the competition rule constraints

3.7 Control System
Transmitter/Receiver: FlySky FS-i6 (6-channel, 2.4 GHz)
Servos: 9 g micro servos (5 units)
Controlled Surfaces: Elevator, rudder, ailerons, container lid
Mixer Configuration: Standard channel mapping (no microcontroller required)

3.8 Stability and Center of Gravity
CG Position: ~25?30% of the wing chord from the leading edge
Static Margin: ~10% for positive longitudinal stability
Balancing: Achieved via battery placement adjustment



3.9 Estimated Specifications

PARAMETER
VALUE
Wingspan
1.0m
Total Length
0.75m
Wing Area
0.18m2
Weight
~900g
Thrust
~0.87kg
Wing Loading
28-30N/m2
*Stall Speed
5.7 m/s
Flight Time
~10-12min
*Based on XFLR5 Simulations




4. DESIGN CALCULATIONS AND ANALYSIS
4.1 Lift Requirement & Stall Speed(Vs)
The aircraft must generate lift equal to its weight at the minimum flying speed (stall condition):			
L = W = (?Vs2?SCLmax??)/2

?Vs  = ?(2W/?SCLmax)

Substituting our aircraft parameters we get:

					     Vs ? 5.8425 m/s

This is acceptable for a hand launched RC plane and ensures low speed stability during takeoff and landing.

4.2 Cruise Speed(VC) and Lift Coefficient(CL)
	A safe cruise speed is typically 1.3?1.5? the stall speed:

					VC  ?  1.5 x VS =  8.76375m/s

	The required CL for this Vc is:

					CL =  2W/?VC2S ?  0.72  ? CLmax=2.1

	This value lies well within the efficient region of the S1223 airfoil, providing both lift and low drag.
4.3 Drag and Required Thrust
	The total drag force at cruise is given by:

					D = (?VC2SCD)/2 ?  0.37N

	The propulsion system must overcome the drag and provide excess thrust for the climb:

					Treq ?  1.3 x D = 0.47 N

	Therefore the required thrust(minimal)  at Cruise: 0.5N
4.4 Power Requirement
Power required for level flight:
Preq = Treq?Vc = 0.47?8.1 = 3.8 W

	Accounting for propeller efficiency(?p=0.75 say):

					Pinput? = Preq/?p?? = 5.1 W

	A 1000?1200 KV BLDC motor on a 3S Li-Po typically delivers >50 W, about 10 times of the required power ensuring ample excess power for takeoff, climb, and maneuvers.

4.5 Center of Gravity(CG) and Stability
	For stable flight, the CG must be slightly ahead of the neutral point:
Typical values for trainer-type aircraft: SM ? 8?12%. CG is thus placed at 25?30% of the chord from the leading edge.
This ensures positive longitudinal static stability ? a restoring pitching moment when disturbed.

4.6 Endurance Estimation
Approximate endurance is calculated from battery energy and average power draw:
Ebatt?=11.1V?2.2Ah=24.4Wh
Assuming average power draw during flight Pavg=70%?80W=56W
t=Ebatt??/Pavg = 24.4/56? = 0.44h ? 26min 

Expected Flight Time: 20?25 min (including partial throttle and glides)



5. Conclusion

The design and analysis of the RC aircraft presented in this report demonstrate a comprehensive approach to achieving an optimal balance between aerodynamic efficiency, stability, and structural strength within the constraints of the Techfest IIT Bombay Aeromodelling Competition 2025. Through iterative calculations, component selection, and material optimization, a high-wing monoplane configuration was finalized to ensure superior stability and controllability during low-speed operations.
The chosen S1223, combined with a 1 m wingspan provides excellent lift characteristics and forgiving stall behavior ? ideal for endurance and payload missions. The propulsion system, centered on a 1000?1200 KV brushless motor with a 3S Li-Po power source, ensures a thrust-to-weight ratio <1(as per rules), granting sufficient climb and maneuvering capability. Structural efficiency is achieved using foam?balsa hybrid construction reinforced with carbon spars, keeping the total weight around 900 g while maintaining rigidity and durability.
Theoretical analysis and stability checks confirm that the aircraft possesses adequate static and dynamic stability, low wing loading, and endurance of over 20 minutes under normal flight conditions. These parameters collectively ensure predictable flight characteristics, ease of control, and mission reliability.
Overall, the project successfully integrates aerodynamic theory, practical design considerations, and hands-on fabrication techniques to produce a capable and competition-ready RC aircraft. With properr testing and fine-tuning, the designed model is expected to perform efficiently across all Techfest rounds, showcasing both engineering precision and innovation in design.
