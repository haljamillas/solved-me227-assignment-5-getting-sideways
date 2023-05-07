Download Link: https://assignmentchef.com/product/solved-me227-assignment-5-getting-sideways
<br>
For this homework, we will study the drift dynamics of Marty, our student-built all-electric DeLorean.

<h1>Instructions</h1>

This homework assignment will be submitted using Gradescope.

All written portions must be turned in through Gradescope. See the Piazza post on homework guidelines for more instructions on the different homework resources available to you. Whatever format you decide to use, please <strong>BOX </strong>all of your final answers.

When completing the assignment, use the set of parameters given to you for MARTY. These are given in Problem 1 of the assignment, as well as the code templates for Problem 2.

1

<h1>Problem 1 – Phase Portraits</h1>

In this problem, we will look at phase portraits of Marty generated using PPLANE, a MATLAB plotting tool for phase plane analysis. There are code and instructions zipped up on Canvas. You will run the script called pplane2017.m. You can either run PPLANE locally or in MATLAB Online.

Parameters you will need for Marty are given in the table below:

<table width="429">

 <tbody>

  <tr>

   <td width="77">Parameter</td>

   <td width="60">Value</td>

   <td width="52">Units</td>

   <td width="240">Meaning</td>

  </tr>

  <tr>

   <td width="77"><em>m</em></td>

   <td width="60">1450</td>

   <td width="52">kg</td>

   <td width="240">Mass</td>

  </tr>

  <tr>

   <td width="77"><em>C</em><em>αf</em></td>

   <td width="60">60,000</td>

   <td width="52">N/rad</td>

   <td width="240">Front cornering stiffness (lumped)</td>

  </tr>

  <tr>

   <td width="77"><em>C</em><em>αr</em></td>

   <td width="60">160,000</td>

   <td width="52">N/rad</td>

   <td width="240">Rear cornering stiffness (lumped)</td>

  </tr>

  <tr>

   <td width="77"><em>µ</em></td>

   <td width="60">1.1</td>

   <td width="52"> </td>

   <td width="240">Front/rear tire-road friction coefficient</td>

  </tr>

  <tr>

   <td width="77"><em>L</em></td>

   <td width="60">2.4</td>

   <td width="52">m</td>

   <td width="240">Wheelbase</td>

  </tr>

  <tr>

   <td width="77"><em>I<sub>z</sub></em></td>

   <td width="60">2300</td>

   <td width="52">kg m<sup>2</sup></td>

   <td width="240">Yaw inertia</td>

  </tr>

  <tr>

   <td width="77"><em>W<sub>f</sub></em></td>

   <td width="60">0.33</td>

   <td width="52"> </td>

   <td width="240">Static front axle weight fraction</td>

  </tr>

 </tbody>

</table>

Table 5.1: Marty Parameters

<h2>Question 1.A – Predicting the Phase Portrait (Gradescope)</h2>

If we use a linear tire model and the linear bicycle model equations of motion for Marty, how many equilibria do you expect to see? Compute the understeer gradient of Marty – based on this, what stability characteristics do you expect for the linear model?

<em>Give a number of equilibria, the understeer gradient, and expected stability characteristics.</em>

<h2>Question 1.B – Linear Tire Phase Portrait (Gradescope)</h2>

Generate a phase portrait for <em>U<sub>y </sub></em>and <em>r </em>and include the result. Is this a stable equilibrium? Explain why.

<em>Include your phase portrait.               Describe whether this is a stable equilibrium.                Explain your reasoning.</em>

<h2>Question 1.C – Nonlinear Tire Phase Portrait (Gradescope)</h2>

Generate a phase portrait for <em>U<sub>y </sub></em>and <em>r </em>and include your plot. How many equilibria are there? How would you classify these equilibria? Are they stable? Explain why.

<em>Include your phase potrait. How many equilibria are there? Describe what types of equilibria these are and if they are stable. Explain your reasoning.</em>

<h2>Question 1.D – Drifting Location (Gradescope)</h2>

Go to the YouTube link <a href="https://www.youtube.com/watch?v=3x3SqeSdrAE">here</a> and watch Marty on the course. First, enjoy how super cool that is. Second, see if you can understand how this works based on what we saw in class.

Which of the equilibria in the phase portrait you generated in Problem 1C corresponds to the drifting condition of turning right to go left? You can see Marty doing this around 40 seconds into the video. Explain why it corresponds to that equilibrium.

<em>Explain which equlibrium corresponds to the described condition and how you know</em>.

<h1>Problem 2 – Simulated Drifting</h1>

Now that we have explored the equilibria of a two-state model with nonlinear tires, let’s see if we can make Marty drift in simulation.

<h2>Question 2.A – Equations of Motion (Gradescope)</h2>

We are going to simulate Marty with a nonlinear bicycle model with lateral velocity <em>U<sub>y </sub></em>and yaw rate <em>r </em>as the two lateral states, and a third state for longitudinal velocity <em>U<sub>x</sub></em>. Since Marty is rear-wheel drive, assume that a longitudinal drive force <em>F<sub>xr </sub></em>is applied at the lumped rear tire (there is no braking force at the front axle), and neglect drag and rolling resistance. What are the (nonlinear) equations of motion? (Do not make any small angle or linear tire approximations)

<em>U</em>˙<em>x </em>=? <em>U</em>˙<em>y </em>=? <em>r</em>˙ =?

<em>Give the nonlinear equations of motion for Marty.</em>

<h2>Question 2.B – Constant Speed From Rear Longitudinal Force (Gradescope)</h2>

The model in PPLANE assumed <em>U<sub>x </sub></em>was constant and we used that to generate the phase portraits. However, our model includes longitudinal dynamics. What value of <em>F<sub>xr </sub></em>allows us to obtain a constant speed of 8 m/s in steady-state? Use the equilibrium lateral velocity and yaw rate you found in Problem 1D with a steer angle of <em>δ </em>= −10<sup>◦</sup>

<em>Find the value of F<sub>xr </sub></em><em>that gives a constant forward velocity of 8 m/s.</em>

<h2>Question 2.C – Simulating from Equilibrium (Gradescope)</h2>

For this problem we will use the simple coupled tire model where <em>F<sub>x </sub></em>is assumed to be known. Incorporate this into your simulation (We will supply verification code). Run your simulation of the three-state bicycle model for 4 seconds using <em>δ </em>= -10° and <em>F<sub>xr </sub></em>equal to the value you computed in Problem 2B. Use the drift equilibrium found in Problem 1D as the initial condition. Plot <em>U<sub>y</sub></em>, <em>r</em>, and <em>U<sub>x </sub></em>on the same plot. Does Marty hold the drift? What happens? Did you expect this? If you’d like, visualize using animateDrift.m.

<em>Include your plot and an explanation of what you see.</em>

<h2>Question 2.D – Drifting Intuition (Gradescope)</h2>

In problem 2.E, you will implement a longitudinal and lateral controller to stabilize Marty in a drift. Let’s think briefly about the forces at play while drifting in this problem. In the case of a left-handed drift (e.g. yawrate is positive), you, the driver, have stabilized the vehicle with a negative steering wheel angle. In each ”Observed Behavior” listed in the table, select the correct input to stabilize the vehicle. When <em>δ </em>is held constant, select the correct <em>F<sub>x </sub></em>trend to stabilize the vehicle. When <em>F<sub>x </sub></em>is held constant, select the correct steering input trend to stabilize the vehicle. Provide an explanation for the input you selected.

<em>Circle the correct δ </em><em>and F<sub>x </sub></em><em>inputs where applicable. Provide an explanation for your choice.</em>

<table width="640">

 <tbody>

  <tr>

   <td width="97">Observed Behavior</td>

   <td width="224"><em>δ</em></td>

   <td colspan="3" width="111"><em>F<sub>x</sub></em></td>

   <td width="207">Explanation</td>

  </tr>

  <tr>

   <td width="97"><em>r </em>too large</td>

   <td width="224"><strong>more negative </strong>/ <strong>less negative</strong></td>

   <td width="69">constant</td>

   <td width="27"> </td>

   <td width="15"> </td>

   <td width="207"> </td>

  </tr>

  <tr>

   <td width="97"><em>r </em>too large</td>

   <td width="224">constant</td>

   <td width="69"><strong>increase decrease</strong></td>

   <td width="27"><em>F<sub>x</sub></em><em>F<sub>x</sub></em></td>

   <td width="15">/</td>

   <td width="207"> </td>

  </tr>

  <tr>

   <td width="97">|<em>U<sub>y</sub></em>| too large</td>

   <td width="224"><strong>more negative </strong>/ <strong>less negative</strong></td>

   <td width="69">constant</td>

   <td width="27"> </td>

   <td width="15"> </td>

   <td width="207"> </td>

  </tr>

  <tr>

   <td width="97">|<em>U<sub>y</sub></em>| too large</td>

   <td width="224">constant</td>

   <td width="69"><strong>increase decrease</strong></td>

   <td width="27"><em>F<sub>x</sub></em><em>F<sub>x</sub></em></td>

   <td width="15">/</td>

   <td width="207"> </td>

  </tr>

 </tbody>

</table>

<h2>Question 2.E – Controlled Drifting (Gradescope)</h2>

To sustain the drift let’s add feedback terms to the values of <em>δ </em>and <em>F<sub>xr</sub></em>. Use a simple longitudinal controlled to track the desired longitudinal speed:

<em>F</em><em>xr </em>= <em>K</em><em>x</em>(<em>U</em><em>X,</em>des − <em>U</em><em>x</em>) + <em>F</em><em>x,ff</em>

Where <em>K<sub>x </sub></em>= 2,000 N/(m/s), <em>U<sub>x,</sub></em><sub>des </sub>= 8 m/s, and <em>F<sub>x,ff </sub></em>is the value you found in Problem 2B. For the feedback steering, using proportional control on <em>U<sub>y </sub></em>and <em>r</em>:

<em>δ </em>= <em>k</em><em>r</em>(<em>r</em>des − <em>r</em>) + <em>k</em><em>y</em>(<em>U</em><em>y,</em>des − <em>U</em><em>y</em>) + <em>δ</em><em>ff</em>

The absolute value <em>k<sub>r </sub></em>= 1 s. The absolute value of <em>k<sub>y </sub></em>= 0.5 rad/(m/s), and <em>δ<sub>ff </sub></em>= -10°. Based on your observations in Problem 2.D, select the sign for <em>k<sub>r </sub></em>and <em>k<sub>y</sub></em>. Simulate for 9 seconds using the drift equilibrium as the initial condition. Plot <em>U<sub>y</sub></em>, <em>r</em>, and <em>U<sub>x </sub></em>and visualize the animation. Are we drifting now? What is the steady state sideslip angle?

<em>Plot of the states with an explanation of whether we are drifting and why. A calculation for the steady state sideslip angle.</em>