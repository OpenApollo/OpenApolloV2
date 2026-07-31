# OpenApolloV2
Repository for OpenApollo V2

The OpenApollo Project strives to lower the barrier of entry for beginners into the world of amateur rocketry and aviaton, by supplying an open-sourced platform, which solves the hardest and most intimidating parts of designing a fast, reliable and redundant circuit.

Designing the flight controller of a rocket is often the most intimidating parts of such a project, as it needs to be absolutely foolproof. It requires in-depth knowledge to make a high-speed servo-gyro feedback loop for flight stabilization, implement redundancy and failure handling, and have it be able to work in harsh conditions.

OpenApollo V2 provides a pre-built, open-sourced platform to make one of the most difficult parts of amateur rocketry more tolerable. Designing low-level control is incredibly difficult for beginners, and OpenApollo solves this by doing that for you, while also providing a Raspberry Pi CM5, which communicates directly with the low-level hardware, making it possible to control an entire flight with easy, high-level code written on the CM5. This separation keeps time-critical control on the microcontroller while allowing complex guidance, navigation, telemetry, or complex algorithms/ML/MV to run on a powerful Linux computer 


V2 upgrades the following from V1:
 - Better and smaller PCB size
 - Faster sensor feedback loops, due to low-level control
 - Easier connectivity for optional external sensors
 - More seperation between high-level and low-level parts, so beginners have to look into low-level parts as little as possible

V2 features the following parts:
 - I3G4250DTR Gyroscope
 - H3LIS200DLTR Accelerometer
 - MS561101BA03-50 Barometer and temperature sensor
 - STM32L412KBT6 as the Servo Feedback Controller [SFC]: Communicates with gyroscope and controls servo motors
 - STM32F745VET6 as the Master Peripheral Controller [MPC]: Communicates with GPS, Barometer, Accelerometer, SFC, Raspberry Pi CM5, and operates 4 high-power MOSFET switches
 - STM32G030F6P6 as a Flight Termination Controller [FTC]: Listens for heartbeats from both STMs, and the CM5, and can reboot both STMs, or trigger emergency protocols, icnluding controlling 3 MOSFET switches
 - Raspberry Pi CM5 running Linux, which can be used for resource-intensive calculations, and to set a flight path or protocols with easy, high-level code
 - HC-12 for telemetry (range can be increased greatly with an optimal 1/4th wavelength antenna)


oshwlab (has not been approved yet, though I'm not sure whether that's even needed):
https://oshwlab.com/ttomiz/project_hppayogv
