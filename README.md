Download Link: https://assignmentchef.com/product/solved-cse271-lab9-a-graphical-application-that-produces-a-restaurant-bill
<br>
<h1></h1>

Write a graphical application that produces a restaurant bill.  YOU WILL NOT BE GRADED ON

LAYOUT/AESTHETICS, unless it is unreadable. Instead, focus ON FUNCTIONALITY AND ADHERANCE TO REQUIREMENTS only.

<ul>

 <li>Provide buttons for ten popular dishes or drink items. You decide on the items and their prices. Optionally, you can use accompanying labels or set the text of the button (8 points, see some implementation options below)</li>

 <li>Provide text fields and a button for entering less popular items and prices. The item will be a separate field from its price, and you will require a button. (3 points)</li>

 <li>In a text area, show the bill as items are entered.</li>

</ul>

Have a button (“Calculate”) that adds some tax and a preset tip, and calculates the total bill after the user clicks a finish/calculate bill button.  (4 points)

Since we have not learned layouts yet, simply add all your components to a single panel and set your frame height and width such that the program appears the most readable and intuitive.

<h3>Button Implementation Options</h3>

There are different ways you can design and implement your buttons. We describe three options here, in order of points that reflect the better designs.

Best Option – Full Points (8/8)

Advanced (best way of doing it) that won’t require you to compare buttons at all (no if statement).  All of these JComponents are extendable, so,

<ul>

 <li>Extend JButton to make your own restaurant button.</li>

 <li>Give it instance variables that you need for your calculations.</li>

 <li>Make a single ActionListener</li>

 <li>Now, when the ActionListener ActionPerformed method is pushed, you can check if the source is an instanceOf YourNewButtonType, cast it to that YourNewButtonType, and use its getters to get the information you need.</li>

</ul>

This is for full points and will make your lives a lot easier, as well as teach an important lesson about inheritance.

Advanced Option (6-7/8)

<ul>

 <li>Make ONE action listener that responds to all 10 menu item buttons.</li>

 <li>Use the parameter of the ActionPerformed method (Event) to find out which button is the source of the event using Event.getSource(). Then compare that to your buttons, which should be instance variables, to find out which button was pushed, and act accordingly. HINT: THIS IS POSSIBLE BECAUSE YOU WILL HAVE MADE YOUR ActionListener in a specific way that that can see these instance variables.</li>

</ul>

CSE 271 – Spring 2017                        Thursday Labs Due Monday 11:59pm

Friday Labs Due Tuesday 11:59pm




Easiest but least points option (4-5/8)

Make 10 different action listeners for each of the 10 buttons.    You’ll know exactly which button is pushed since it’ll go directly to that listener, but it’ll be poorly organized and too much code.

<h3>Tips</h3>

Also, for full points, you should be breaking down long methods (including a constructor) into smaller, private, helper methods. We have tons of examples of this from this past week in the canvas module. Use those as a starting point/reference, and modify for your own purposes.

You have the choice of having a “main” in your extended Frame to kick off your program, or you can have a separate class to run your frame, like we did in lecture. Your choice!

<h2>Part 2 (15 points)</h2>

Write a program that displays the Olympic rings as shown below.

To accomplish this, create and use a method <sub>drawRing</sub> that draws a single ring of a given (parameter) position and color. (10 points) You must use this method 5 times to create your Olympic rings!

Color the rings in the provided Olympic colors. (5 points) Note, that these rings may be thicker than yours. You are allowed to do thin rings.













<h3>Tips</h3>

Your “drawRing” helper method is allowed to have Graphics G (from the paintComponent method) as a parameter.