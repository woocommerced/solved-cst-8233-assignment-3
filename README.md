Download Link: https://assignmentchef.com/product/solved-cst-8233-assignment-3
<br>
<h1> Martian Lander</h1>

<strong>Purpose: </strong>Solve Ordinary differential Equations (ODEs) in real-time for a planetary lander flight simulator.

<strong> </strong>Algorithm

While the user wishes to continue, the application will ask the user to select whether to run the simulation one more time. The simulation uses Heun’s adaptation of Euler’s method, as explained in lecture notes, to solve the following differential equations that describe the descent of a landing module on Mars under gravity with atmospheric drag and an additional booster term B:

dv/dt = g – c*(v + a*(v/vmax)<sup>3</sup>) – B v = dx/dt




The values of the constants are g = 3.7, c = 0.13, a = 8.3, vmax = 46

Solving these equations means calculating the velocity v and position x of the module as time t (seconds) passes after it starts its descent from an initial location 1000 meters above the Martian surface at the instant of being released from the mother ship. It then falls to the surface under the above equations.

The meanings of the terms are:

<ol>

 <li>dv/dt in the acceleration of the lander module as it falls to the surface where v (in metres/second) is positive in a downward direction. At the instant of release v is zero and x is 1000 metres and time t (in seconds) is zero. Time is measured from the computer clock.</li>

 <li>g is the downward acceleration caused by gravity (which on Mars is only 38% of Earth’s gravity).</li>

 <li>c*(v + a*(v/vmax)<sup>3</sup>) is the deceleration caused by atmospheric drag. It is small when the velocity is small and gets large as a power law as the velocity increases. At some high velocity (called the terminal velocity) it balances gravity and acceleration becomes zero..</li>

 <li>B is the deceleration cause by a burn from the braking rocket on the landing module. This always acts in an upward direction to counter gravity. This rocket can be turned on and off and adjusted from the keyboard using the keys W (increases B) and E (decreases B). However, braking uses up fuel at the rate of B units per second and so depletes the fixed reserve of 100 units.</li>

</ol>




When the simulation starts, the lander is 1000 meters above the Martian surface at the instant of being released from the mother ship. It then falls to the surface under the above equations. The purpose of the simulation is to get a soft landing which is taken as a speed of &lt; 1metre/sec at a distance above the surface of &lt;1 metre. If the module hits the surface faster than this it gets bounced back up again (v becomes –v) until gravity pulls it down again. The best landing is a straight descent without a single bounce. The number of bounces is recorded. Try to land without a single bounce.




There is a “bare-bones” console executable <em>lander.exe</em> in a zip file on BS that runs the simulation as a single shot – it does not offer a repeat and does not save the results to file. Your version should work the same and display the same information in the same way. In addition add the following:

<ol>

 <li>offer the user the option of repeating the simulation</li>

 <li>save the results of all simulations to file and display them on-screen at the end in order of best-toworst landings together with the name of the user. The best is shortest time with fewest bounces.</li>

</ol>

<strong> </strong>

Set up a Win32 console project in Visual Studio 2015 with the name ass3. In a file named ass3.cpp using the C (or/C++) programming language write the code to implement the application as described above. Remember to implement the Heun improvement – not just the Euler method.




1







<strong>CST 8233  F18  Assignment 3 </strong>







See the Marking Sheet for how you can lose marks, but you definitely lose 60% or more if:

<ul>

 <li>your application won’t build in Visual Studio 2015</li>

 <li>your application crashes in normal operation</li>

 <li>I can’t build it because you submitted the wrong files or the files are missing, even if it’s an honest mistake – 100% deduction.</li>

</ul>

<strong> </strong>