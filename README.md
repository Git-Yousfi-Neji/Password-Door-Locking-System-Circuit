# Password-Door-Locking-System-Circuit<br />
A door lock project based on a Arduino board<br />

I’ll use for the lock a solenoid and a relay, it depends on your lock system you’ll have to chose a wiring, codes and adapt them.<br />

 **N.B: For a real project, I don’t recommend using a solenoid at all, but rather hack a lock that can be opened by both electronic and mechanic lock and adapt your project for it.**<br />

**PARTS**<br />
So for this project we will need those components, alongside some jump wires, and a power supply of 12V Sorry I didn’t add it here:

<img src="../main/parts/1.png?raw=true" ><br />
<img src="../main/parts/2.png?raw=true" ><br />
<img src="../main/parts/3.png?raw=true" ><br />
<img src="../main/parts/4.png?raw=true" ><br />
<img src="../main/parts/5.png?raw=true" ><br />
<img src="../main/parts/6.png?raw=true" ><br />
<img src="../main/parts/7.png?raw=true" ><br />
<img src="../main/parts/8.png?raw=true" ><br />

The Push Button is meant to open the lock from inside, you can remove it if you want, the resistor is for debounce.

I used 4×4 Keypad you can use 3×4 but you’ll need to modify somethings in the code like for confirmation I use ‘A’ you can change it to ‘*’ or ‘#’.

The solenoid is powered by 12V external power supply, and driven by the IRF510N MOSFET transistor.

The Transistor is used as a switch and it’s better to use an N-channel, the IRF510N is pretty popular when used with an Arduino, when you apply a 5V voltage across the Gate and the Source, the transistor becomes like a closed switch between the Drain and the Source, and it doesn’t need any resistor like bipolar ones.

And if there’s no voltage applied the transistor acts like an open switch, and this how we control the solenoid.

For the other example I’m using a 1 channel  relay module, it works with 3.3V, and we control its input like controling the transistor, the only difference is that they are inverted

***N.B: You can use the relay to control any electric lock up to 250VAC, you can use it also to control the Solenoid…***

The codes are exactly the same the only thing is that you switch between (LOW and HIGH) to open the lock.

Just remember first time you must upload the code and change the passcode then uncomment some lines (read the code to find them (they’re in setup)) and reupload the code so it can read the passcode from the EEPROM.IT’S DONE ONLY ONCE.

Also you can change the code length, first I made it four digits, you can change it from the default code, as I used in the code the "sizeof(code)" instead of "4". You can't change a 4 digits code to a 6 digits passcode, first change the initial passcode from the code source.

**TEST**<br />
You'll find the test in pictures below, navigate though them
<img src="../main/test/1.png?raw=true" ><br />
<img src="../main/test/2.png?raw=true" ><br />
<img src="../main/test/3.png?raw=true" ><br />
<img src="../main/test/4.png?raw=true" ><br />
<img src="../main/test/5.png?raw=true" ><br />
<img src="../main/test/6.png?raw=true" ><br />
<img src="../main/test/7.png?raw=true" ><br />
<img src="../main/test/8.png?raw=true" ><br />
<img src="../main/test/9.png?raw=true" ><br />
<img src="../main/test/10.png?raw=true" ><br />
<img src="../main/test/11.png?raw=true" ><br />
<img src="../main/test/12.png?raw=true" ><br />

**SCHEMATICS: **<br />
**Mosfet + Solenoid wiring**<br />
<img src="../main/schematics/mosfet_solenoid_wiring.png?raw=true" ><br />
**Relay wiring**<br />
<img src="../main/schematics/relay_wiring.png?raw=true" ><br />

Well that was the test of the project, it’s the same for the solenoid or relay, and the push button opens from the inside if you want or you can remove it.
