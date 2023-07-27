

## The Type Of The Drone

- The best drone for beginners is the **5" drone**.


## The Frame

![[Pasted image 20230715104841.png]]
- The width of the drone (distance between the front motors): 135 mm.
- The height of the drone (distance between the side motors): 173 mm.
- The diameter of the drone (distance between the opposite motors): 219 mm.

![[Pasted image 20230720151219.png]]

- The thickness of the arms should be at least 4 mm thick.
![[Pasted image 20230715105604.png]]
- The best frame shape is probably the **True-X** shape.
- Unibody design? Not sure, will have to do some research on how to make the arms separate.
	- When the arms are separate from the frame, they can be fixed more easily.
- The best material for the frame would be carbon fiber, but since **Original Prusa Mini+ Kit** does not support that, the next thing is PETG.
- For beginners, the frame should more like an freestyle frame, because it can take more damage, and it is more easy to work on when crashed.
- When build a freestyle drone, **the battery** should come on top of the drone. It is not optimal for performance, but it protects the battery in most crashes.

## The Brushless motors

- Motor size is typically noted in a **XXYY** format with the first two digits referring to the **stator diameter** in *mm* and the second two being the **height of the magnets**.

- **KV** stands for **motors velocity constant** which means how many RPM per volt the motor can give for example a 2300kv motor at full throttle on 10V would be spinning at 23000rpm.



- Recommended stats for 5" sized drone:
	- Stator size: 22 - 23
	- Magnet height: 05 - 07
	- Motor KV: 2200 - 2800
	- ESC size:  20 - 35A.

## The ESCs

- Also known as **electronic speed controllers**.
- Produces the three phase AC current needed to drive the motors.
- Two possibilities:
	1. Four separate ESCs to mount them on the arms.
	2. All in one board that sits inside the frame (if the frame still has space for that).
- **REMEMBER to calculate the amp draw of the setup!!**. The ESCs need to burst current to exceed the motor amp draws or they could burst into flames up mid flight!
- ESCs are reasonably intelligent and can run on different software. Should consider ESCs running **BIHeli_S** or **KISS ESCs**.

## The Flight controller

- Is the brain of the drone taking into account the angle of the drone and the control input in calculates how fast the motors should spin and sends the signals to the ESCs.
- Normally built for certain software such as **BIHelo_S** or **KISS**.
	- The cheapest and most popular option is currently **Betaflight**, and **KISS**.
- When checking the processor, pick either F3 or F4 chip.


## The Power Distribution Board

- The **PDB** takes the battery voltage and provides various points for connecting up all other electronics.
- Should contain voltage regulators or BECS so the drone won't burst into flames.

## The Drone Propellers

- Propellers "Props" are often denoted as a AxBxC where A is the size in inches, B is the pitch (angle of the prop) and C is the number of the blades.
- The most common amount of blades is three.
- The higher the pitch of the prop the faster the drone can go but at the same time your motors will draw more current pushing the electronics harder and draining the battery fast.

## Radio Transmitter And Receiver

- Every radio talks in their own protocol. Recommended protocols are either SBUS, IBUS, DSm2 and DSMX.

## Some Sources

- https://dronenodes.com/how-to-build-a-drone/
- Some recommendations for brushless motors: https://dronenodes.com/drone-motors-brushless-guide/
- https://www.getfpv.com/armattan-chameleon-ti-5-frame.html?cmid=eHZ3Y2tBWGYrQWM9&ats=R2h2YTNRZFdsbkU9
- https://www.circuitbasics.com/wireless-communication-between-two-arduinos/
- https://www.utmel.com/components/l9110s-2-channel-motor-driver-circuit-pinout-and-how-to-work-video-faq?id=1988
- https://ozeki.hu/p_2987-how-to-use-a-gyroscope-sensor-in-arduino.html
- https://www.instructables.com/How-to-use-a-Buzzer-Arduino-Tutorial/

## Possible Parts

- [ ] Brushless motors: https://www.hobbylinna.fi/fi/product/xrotor-1408-race-pro-fpv-motor-2850kv-5s/HW30405551?gad=1&gclid=CjwKCAjwh8mlBhB_EiwAsztdBCjKQRsyOBbffTZDJmQ97w4sMmI7H-hxsi9QkvCFAkzV2e212S2JmhoCCvAQAvD_BwE 24.20€
- [X] RF transmitter: https://www.spelektroniikka.fi/p24048-nrf24l01-24ghz-tx-rx-module-langaton-lahetin-vastaanotin-fi.html 4.00€
- [X] DC Motors: https://www.partco.fi/fi/saehkoemekaniikka/moottorit/dc-moottorit/17174-mot-12v-6600.html 4.50€
- [X] Motor controller: https://www.partco.fi/fi/robotit/robottielektroniikkaa/19348-4tx-l9110s.html 6.50€
- [X] Gyroskope: https://www.spelektroniikka.fi/p23829-gy-521-mpu-6050-3-akselinen-gyro-ja-kiihtyvyysmittari-arduinolle-fi.html 8.20€
- [x] Joystick: https://www.spelektroniikka.fi/p20358-joystick-moduuli-ky-023-arduinoon-tai-muualle-analoginen-10k-trimmerit-painonapp-fi.html 3.00€
- [x] Piezo: https://www.spelektroniikka.fi/p14441-piezosummeri-johdoilla-4-20vdc-ps20-fi.html 2.50€
- [x] Battery holder: https://www.spelektroniikka.fi/p17988-paristonpidin-paristokotelo-9v-johdot-kotelon-paassa-fi.html 1.00€
- [x] Battery: https://www.puuilo.fi/varta-akkuparisto-6hf22-9v-200mah-1kpl 13.90€
- [x] Arduino Mega: https://www.partco.fi/fi/arduino/arduino-kloonit/19220-ard-mega2560r3.html 36.60€
- [ ] Screws: https://www.bauhaus.fi/kiinnitysruuvi-abb-3-x-16-mm-100-kpl.html
- Toimituskulut partco: 6.90€
- Total: 
	- $2 * 4.00€ + 2 * 4.50€ + 4 * 6.50€ + 8.20€ +6.90€ + 2 * 3.00€ + 2.50€ + 1.00€ + 13.90€ + 36.60€ = 118.10€$


## The Currents

- The four motors draw $4 * 40mA = 160mA$ (12V).
	- The max amount they can take is 1A.
- The motor controller gives 800mA per channel.


## Files

- The Schematic files can be found from [[/home/eme/LibrePCB-Workspace/projects/Drone]].
