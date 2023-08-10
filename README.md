# Water Sorter Puzzle Solver - C# Project
## Introduction
#### Author: Steve Tamayo
This project was made in Visual Studio from August 2022 - September 2022. The application finds the solution to a water sorter puzzle in the least number of steps using heuristic programming. The application can also create random tubes based on three common factors found in water puzzles: number of different colors, number of empty tubes, and how many segments of water can fit in a tube (the application refers to a segment as "section"). Finally, the application allows the user to customize the water puzzle to any legal configuration.

**Quick Note: The application has certain limits in place for the solver discovered through testing:**
* You can have a minimum of 2 colors to a maximum of 15 colors.
* You can have a minimum of 2 empty tubes and a maximum of 4 empty tubes
* You can have a minimum of 3 sections and a maximum of 5 sections
* If the solver tries to come up with a solution and fails, if the minimum number of empty tubes is below 4, it will ask if the user would like to add an empty tube and rerun the solver.

## What is a Water Sorter Puzzle?

There are many different versions of this idea out there, but the basics are that you have multiple containers (in this application refered to as "tubes") with sections of water that have been mixed up. You can move the top most color of a tube to an empty tube or another tube with an open section, as long as the color you are moving matches the top most color in the receving tube. *In this application, two or more touching colors move as a singular unit with one step. You cannot split up touching colors after joining them.* You repeat this process until all colors are each matched in a singular tube.

An example of movement in a Water Sorter Puzzle (using this application UI:
<!-- Insert GIF of an example game zoomed in> -->

# Using the App (Main Window part 1)

When opening the app, you have main window. I'll focus on the right section for now. 

At the top, this section displays the puzzle configuration (further refered to as "puzzle display"). In the bottom right is the "Check For Solution" button, which will have the application determine the solution for the puzzle in the least number of steps. 

<!-- Insert GIF of mouse circling the top section (no solution shown), then the Check for Solution section, click the Check for Solution button-->

When a solution is found, the section under the "puzzle display" will fill with text saying how many steps the solution takes. Under that will be a collection of buttons that show each step of the solution. "Start" shows the initial puzzle configuration. Each following button will have text in a "X->Y" format, with "X" being the tube the top color is being taken from and "Y" being the tube receiving that color. Clicking each button will show that step of the solution with the last being the tubes solved.

<!-- Insert GIF of mouse circling the solution text, then the steps button container, then clicking every step until the solution -->

At the bottom left of this right section are two other buttons: "Random Tubes" and "Edit Tubes". "Random Tubes" will randomize the puzzle configuration in the "puzzle display" based on three editable factors above it (number of colors, number of exmpty tubes, number of sections). You can then hit the "Check For Solution" button as normal to find the solution to this randomized configuration.

<!-- Insert GIF of mouse clicking the Random Tubes button, then circling the editable factors about it, then clicking the Rnadom tubes button, then finally the check for solutions button -->

Finally the "Edit Tubes" button wil open a new window called "Input Tubes." Here you can customize the puzzle configuration. I go over this window in the next section.

<!-- Insert GIF of mouse hitting "Edit Tubes" and opening the Input Tubes window -->

