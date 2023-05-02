---
Title: Lessons Learned and Future Recommendations
---

## Lessons Learned

1.	Make sure your team identifies an effective, open communication channel that everyone can use. The most critical part of team work is communication. Discord is an excellent communication tool if your team is looking for one. 
2.	Cadence libraries are fickle and need to be very well fine tuned to work properly. Take steps to ensure libraries are configured properly before going into the design stages.
3.	Design footprints with larger pads to be easier to solder. This also helps with ensuring no continuity problems.
4.	Lean towards going above minimum ratings for traces, because smaller traces are much more delicate and prone to damage.
5.	Keep records of previously built circuits, whether it be photos or schematic designs. This will help with debugging more complex circuits later.
6.	Although team responsibilities are broken down into subsystems, it’s critical each team member understands the fundamentals of each subsystem. It’s easier for teammates to help if they understand the basic functionality of each subsystem.
7.	Solder Mask layers do not completely save the board from poor solder jobs. Ensure that there are no issues with shorts or continuity before powering your boards.
8.	Include as many debug layers as possible on the board. This includes debug LEDs on outputs for things like a motor driver, or adding test points to every trace. This is going to be a tedious and laborious process in early design, but will save more time in the long run.
9.	Ensure that the PIC that is chosen is compatible with the rest of the subsystems on the board. The amount of memory a PIC has is often overlooked, but can cause issues later if not considered.
10.	DO NOT delete anything from previous report sections. Keep all the information in some type of repository so that it can easily be accessed and adjusted to re-add to any relevant sections of the reports. 

## Recommendations for Future Students

1.	Ask your peers for assistance when needed. Your peers are seeing the same challenges as you, don’t be afraid to ask for aid. Oftentimes, you may find that troubleshooting issues you are having with another person on the same sub system is the best way to learn the material.
2.	Make sure your footprints are the correct size before you go through the manufacturing process. DRC doesn’t tell you the footprint is too small, you are often best off asking the teaching team to review your design before going through the board fabrication - this will save you stress in the future. 
3.	Getting a second opinion on your design choice is a good way to ensure that you are on the right track. Don’t hesitate to just show a peer your design and ask “is there something I can do better here?” You may find that they point out obvious things you missed, such as certain connections being wrong on the design or a backwards diode. Even a single second look can make a world of difference
4.	Build a backup board when the time comes for final manufacturing. This means you will need to buy extra components, but having a backup board will save you a lot of headache if you run into issues on your main board. 
5.	Any circuit you build is worth taking a picture of. If you need to rebuild the circuit later, having a picture as a reference can save you a lot of time. It’s often best to breadboard out something you know worked before as a means of debugging a subsystem later on in the project.

[Back to Project Overview](index.md)
