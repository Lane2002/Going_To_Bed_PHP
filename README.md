# Going_To_Bed_PHP
LEARN PHP
Going to Bed
This project provides practice for:

Creating objects from classes
Writing and using methods
Using static methods
Tasks
17/17 Complete
Mark the tasks as complete by checking them off
Make a Helper Class
1.
In this project we will be creating some pajamas for barnyard animals. The farmer has a special way that she likes names formatted. To ensure this, we are going to build our own string function similar to PHP’s built in strtolower or strtoupper.

We’re going to put this function inside of a helper class StringUtilities (making it a method). We can then add other string utilities or reuse this class in another project for the same farmer.

Begin by creating a StringUtilities class.


Stuck? Get a hint
2.
The farmer likes names to be entirely lowercase, except for the second letter, which should always be uppercase.

Define a method called secondCase inside of StringUtilities which accomplishes this. This method should be static since we won’t be instantiating StringUtilities. We are only using it as a helper class.


Stuck? Get a hint
3.
Test this method by invoking it statically with some strings and printing the results to the screen. There is a case that causes an error, can you find it?


Stuck? Get a hint
4.
While “Q” might not be a popular name, we might use StringUtils in a different application in the future and our method should handle single characters gracefully.

Modify secondCase so that it does not generate an error for:

echo StringUtils::secondCase("Q"); #should print "q"
echo StringUtils::secondCase(""); #should print an empty string

Stuck? Get a hint
Pajamas Already
5.
Now that we have our helper class, we are ready to start making pajamas.

Create a Pajamas class. It should have 3 private properties:

owner
fit
color

Stuck? Get a hint
6.
Add a constructor class for Pajamas. It should allow 3 arguments to be passed in corresponding to the 3 properties we just defined.

Provide defaults for each argument (of your choosing).

Make sure to assign the passed in values to their corresponding properties. Use secondCase in the StringUtilities helper class to ensure that the owner property is properly formatted.


Stuck? Get a hint
7.
We want to be able to describe each Pajamas object.

Add a public describe method which returns a string using the 3 properties to tell us about the object.


Stuck? Get a hint
8.
Now we have enough that we can begin testing our class out. Create an instance of the Pajamas class for “CHICKEN”. Assign it to the variable chicken_PJs. Use your favorite color and fit.

Print the result of using the describe method on chicken_PJs.


Stuck? Get a hint
9.
Let’s say something happened to chicken’s pajamas to change the fit. Like maybe they were washed many times and shrunk. Since fit is a private property, we need to make a setter.

Create a public method setFit which can be used to modify the fit of the pajamas.


Stuck? Get a hint
10.
Now test the setFit method by tightening up chicken’s PJs. Be sure to print the result.


Stuck? Get a hint
A Specialized Type of Pajamas
11.
Some animals need their pajamas to have buttons so that they can put them on.

Create a new class ButtonablePajamas that inherits from Pajamas.


Stuck? Get a hint
12.
We’ll need a new private property, button_state, to maintain the status of the buttons (“buttoned” or “unbuttoned”).

Add this property to ButtonablePajamas and set it to "unbuttoned".


Stuck? Get a hint
13.
The describe method makes no mention of buttons, but it seems like the right place for a message about the buttons.

Within ButtonablePajamas, override the describe method. The version for this class should include a statement about whether the pajamas are buttoned or not.

Remember that you can reuse the parent method with parent::describe() and concatenate the statement about the buttons.


Stuck? Get a hint
14.
Let’s test this class on an animal that definitely needs buttons. Create an instance of ButtonablePajamas with the owner "moose" and save it to the variable $moose_PJs.

Use the describe method to ensure that it let’s us know the pajamas are unbuttoned.


Stuck? Get a hint
15.
Moose would like to close his pajamas, but button_state is private. Create a method toggleButtons that flips the state of the buttons. It should take no arguments.


Stuck? Get a hint
16.
Make sure to check that this method works as expected. Print the result.


Stuck? Get a hint
Beyond
17.
Congratulations on creating some object oriented pajamas!

If you’d like additional practice, you can keep expanding the project. Here are some ideas:

A class of pajamas that has a hat
Performing validation on setFit to only allow “tight”, “fine”, and “loose”
Setter and getter methods for the owner and color properties
