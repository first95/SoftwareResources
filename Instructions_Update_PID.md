## How to Update PID Parameters

Each of our sub-systems with closed-loop control has PID parameters that can be tuned to have improve that control. These sub-systems are the elevator, the cargo handler wrist, and the hatch ground loader wrist (not yet in develop). The parameters are:
- P: proportional, how strong of a response should be made to an error in the controlled variable (position or speed)
- I: integral, how much to penalize an ongoing error (e.g. a small error that persists over time)
- D: derivative, how much to react when the sign/direction of the error changes
- F: feed forward; we're not using this so keep it zero
- I Zone (not a standard parameter): re-set integral term when the error is larger than this so that the integral term doesn't get too big

Here's a reference on PID that may be helpful (or may be too much information). https://www.crossco.com/blog/basics-tuning-pid-loops

### Non-Computer Parts of Process
1. Start with all parameters other than P set to 0, and P set to be a small value (e.g. 0.01).
2. Test the sub-system in question in it's closed-loop mode with these parameters and observe its behavior.
3. If the controlled variable (speed or position) doesn't reach its desired set point or reaches it slowly and with no oscillations, double the P value and repeat.
4. If the controlled variable reaches its desired set point but with significant oscillations, reduce the P value. If the oscillations are very large, reduce it by half; if they're manageable, reduce it by 10%.
5. Repeat until the set point is achieved without large oscillations and at a reasonable speed.
6. Move onto the the integral control. Start with I set to 0.01*P, and test that. If the set point is reached slowly, try increasing I (e.g. doubling it), but reduce it back if it causes oscillations.
7. For our purposes, unless you know what you're doing, you can leave the derivative term (D) at zero. A non-zero D term can enable stablization of oscillations so that a larger P can be used, but can be more difficult to tune.

### Where to Find PID Parameters in Code
Make sure that the appropriate code is checked out on the computer you're using.
1. Open Sourcetree.
2. In the FRC 2019 tab, on the left panel, make sure that the branch "develop" is in bold (means it's checked out).
a. If it's not, MORE HERE... (including checking for uncommitted code)

The PID parameters are generally preceeded by "K_" in our code, e.g. "K_P" for the proportional term, except I Zone, which is I_ZONE. These parameters can be found in their sub-system file -- same name as the sub-system, located at git_repo_location\FRC2019\src\main\java\frc\robot\subsystems. On one of the computers with the programming software (e.g. ones that end in -01 or -02), you can open VSCode (typically a small "W" icon on taskbar) and from the file explorer tab on the left, can navigate to the desired file. When you're done editing it, 

### How to Update Code on the Robot
