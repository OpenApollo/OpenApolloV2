# OpenApolloV2
Repository for OpenApollo V2

The OpenApollo Project aims to lower the barrier to entry for amateur rocketry and experimental aviation by providing an open-source hardware and software platform that removes much of the complexity involved in designing reliable flight electronics

For many beginners, the electronics are one of the most intimidating parts of a project. A flight computer must operate reliably in harsh conditions, tolerate failures where possible, and incorporate appropriate safety features and redundancy. Designing such a system from scratch requires significant knowledge of embedded systems, PCB design, sensor fusion, and real-time software.

OpenApollo solves this by providing a pre-designed, open-source flight controller with a robust hardware platform and reusable low-level firmware (coming soon to V2 lol). Rather than spending months implementing sensor drivers, hardware abstraction layers, communication interfaces, and control loops, users can focus on writing high-level mission logic on a Raspberry Pi Compute Module 5. This separation keeps time-critical control on the microcontroller while allowing complex guidance, navigation, telemetry, or experimental algorithms to run on a powerful Linux computer

Compared to V1, OpenApollo V2 features:

 - A cleaner system architecture
 - A smaller, more compact PCB
 - Faster control and sensor feedback loops
 - Easier expansion for optional external sensors and peripheral control
 - Better separation between low-level real-time control and high-level mission software.

V2 features the following parts:
 - I3G4250DTR Gyroscope
 - H3LIS200DLTR Accelerometer
 - MS561101BA03-50 Barometer and temperature sensor
 - STM32L412KBT6 as the Servo Feedback Controller [SFC]: Communicates with gyroscope and controls servo motors
 - STM32F745VET6 as the Master Peripheral Controller [MPC]: Communicates with GPS, Barometer, Accelerometer, SFC, Raspberry Pi CM5, and operates 4 high-power MOSFET switches
 - STM32G030F6P6 as a Flight Termination Controller [FTC]: Listens for heartbeats from both STMs, and the CM5, and can reboot both STMs, or trigger emergency protocols, icnluding controlling 3 MOSFET switches
 - Raspberry Pi CM5 running Linux, which can be used for resource-intensive calculations, and to set a flight path or protocols with easy, high-level code
 - HC-12 for telemetry (range can be increased greatly with an optimal 1/4th wavelength antenna)
