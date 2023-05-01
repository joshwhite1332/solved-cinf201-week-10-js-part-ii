Download Link: https://assignmentchef.com/product/solved-cinf201-week-10-js-part-ii
<br>
Last week, we learned about JavaScript and how we can use it on our pages to add interactivity to them. This week, we will cover more concepts in JS and how to work with buttons and forms. At the end of this week, students will be able to retrieve input from forms and use it to create output on the HTML page itself.

Previous Participation Questions/Responses

There were no participation questions from last week. Instead, you had to demonstrate that you made progress on an assignment or something related to the Final Project for this course.




This link has the responses to the fun questions from previous weeks. Feel free to look over the responses from myself and your peers.

<u>https://docs.google.com/spreadsheets/d/1QLoQzbO-</u>

<u>Er7ARIECl0aPvY1lKUyZTdYeuwsn4g0XEAk/edit?usp=sharing</u>

<h2>Midterm</h2>

You don’t need to have perfectly placed or finalized content. However, your pages should be mostly put together. Major headings should be used to describe content. If you haven’t thought of text to use, feel free to Google “Lorem Ipsum” for place holder text. You can also use place holder images by Googling those as well. The most important thing is that you have some sort of content placed for your Midterm.

The basic-page-example.html file provided earlier in the semester is a good an example of an acceptable page. Feel free to use some of the CSS I’ve provided (row class, float items to the left, give them a width) to help style your pages. The overall structure should be original and your own work though.

For the Midterm submission, you’ll submit 3 links in total. Each link should point to a different page of your midterm. When I check your work, I should be able to go from page to page easily by using links on your pages.




<strong>What’s Due? </strong>

<ul>

 <li>Participation Proof</li>

 <li>JS Challenges 2 (CW/HW)</li>

 <li>Midterm</li>

</ul>




<h1>More JS Concepts (Lecture/Class Activity)</h1>

<h2>Variable Scope</h2>

In JavaScript, there are two major types of scopes for variables, local and global. Global variables are ones declared outside of functions while local variables are declared inside of functions.




The difference is that global variables can be accessed anywhere in the document. Local variables can only be manipulated inside of their function. In the example below, x is a global variable and y is local to “myFunction()”…this means we can use the x value in and outside of the function. However, we can only refer to y inside of the function it was created in.




var x = 5; // Globally declared x variable var myFunction = function() {

var y = 4; // Locally declared y variable

console.log(x); // X can be accessed inside this function

}

myFunction(); // Produces output

console.log(y); // Will cause an error because y is only defined inside of myFunction

<strong> </strong>

There is also <strong>block scope</strong> which is when a variable is declared inside of a block of code. If that same variable name exists as a global variable, changing its value inside of a block will change the value of the global variable. In the example below, we declare x to be 5 and log it to the console. After that, we check to see if x is greater than 0, if it is, we redeclare it to be 4.




var x = 5;

console.log(x); // Will log 5

if (x &gt; 0) { var x = 4; // Redeclare our variable

}

console.log(x); // Will log 4 since the value has been changed




Sometimes this is what we want, however, there are cases where we want to use the same variable name inside of a block of code without changing the value of the global variable. We can do that by using the <strong>let </strong>keyboard. Instead of using var x = 4, we can use let x = 4.

var x = 5;

console.log(x); // Will log 5

if (x &gt; 0) { let x = 4; // Declare our variable using <strong>let</strong> instead of <strong>var</strong>

} console.log(x); // Will log 5 this time since using let doesn’t affect our global variable.




In the example above, I used let instead of var to declare a variable. As such, the global variable isn’t affected even though I used the same variable name. For the most part, we will deal with function/global variables and won’t need let but it’s a good thing to understand.




<h2>Arrays</h2>

Think of these as lists of any kinds of data (which can include other arrays). These data pieces are separated by commas and placed inside of square brackets. Every item inside of an array has an index number which is used to refer to that item. For example, we might have an array of house pets:




var housePets = [];




The one above is empty and has nothing in it.




var housePets = [‘cat’, ‘dog’, ‘bird’, ‘chinchilla’]




The above array has <strong>four</strong> items, but the index number only goes up to <strong>three.</strong> This is because the first item in any array has an index number of 0. The values are listed below:




housePets[0]; // Refers to cat housePets[1]; // dog housePets[2]; // bird

housePets[3]; // chinchilla




You can change values at any point by referring to the item and then assigning it a new value:




housePet[3] = “fish”;




The array would now be housePets[‘cat’, ‘dog’, ‘bird’, ‘fish’]




Like strings, arrays have their own set of methods/functions which can be used on them.




Using housePets.length; would produce 4 for our case.




We can also use things like pop() or push() to remove or add items to our array.




housePets.pop(); // Removes last item in our array – becomes cat, dog, bird

housePets.push(‘cow’); // Adds cow to the end of our array – becomes cat, dog, bird, cow




Overall, you should think of a variable as a box which holds a value. An array is like a box which contains many other boxes inside of it.

<strong> </strong>

<h2>Objects</h2>

These are things in JS that have their own properties and methods which can be called upon using something called <strong>dot syntax</strong>. Dot syntax is used between objects and functions so that your code knows what to do.




For example, if you have a car, that car has multiple characteristics and things it can perform. We can create an object for a car with the following code:




var myCar = {

name: “Herbie”;          owner: “none”;            age: 58;

honk: function() {alert(“HONK HONK!”);}

};




All you need to do is say var variableName = {} and place all methods/properties inside of the curly brackets. Name, owner, and age are all properties while honk is a method. We separate these with a colon but refer to them as key/value pairs. To get these values and use them, we use <strong>dot syntax</strong> which utilizes a period and the property/method name.




console.log(myCar.name); // Refers to the name key but logs the value “Herbie” to the console

myCar.honk(); // Would cause an alert to appear with “HONK HONK!” myCar.age; // Refers to the age key and the value of 57




Objects in JS are powerful because almost everything is an object of some sort. Arrays, strings, and other types all have their own properties or methods (length, concat, push, pop, splice, etc.).




We have already worked with objects before. One example we have already seen is the console object. We can use the “log” method/function to create output in the Console.




console.log(“Hello World!”);




Console is the object we are using and then we place a period after it to signify that we are going to reference some method/function or property. In our example, we are using the log <strong>function</strong> and then providing “Hello World.” as the <strong>value</strong> for that function.




Similarly, we can do the same with strings or any other object in JS. In the example below, we create a string with a value of “Chris.” After this we create another variable which uses our previously defined string (myName) and the length <strong>property</strong> to get the length of that string. Just like with console or other objects, we use a period to separate the object and the method/function or property.




var myName = “Chris”; // Creates a string with a value of Chris

var myNameLength = myName.length;




<u>Online Resources</u>

<ul>

 <li><u>https://www.w3schools.com/js/js_let.asp</u> (Let vs var)</li>

 <li><u>https://css-tricks.com/javascript-scope-closures/</u> (Only up to “function hoisting”, this goes very in-depth)</li>

 <li><u>https://www.htmldog.com/guides/javascript/beginner/arrays/</u> (Arrays)</li>

 <li><u>https://developer.mozilla.org/en-</u></li>

</ul>

<u>US/docs/Web/JavaScript/Reference/Global_Objects/Array</u> (Array Methods – ignore let for now)

<ul>

 <li><u>https://www.htmldog.com/guides/javascript/beginner/objects/</u> (Objects)</li>

 <li><u>https://www.geeksforgeeks.org/objects-in-javascript/</u> (More Objects)</li>

</ul>




<h2>Working with the DOM</h2>

Follow along with me in a text editor as I demonstrate how to interact with items on the page. If I’m moving too fast, feel free to look through the code in today’s class examples. I’ve provided links to them below. Most of the work I do during my live demonstration will be pulled from these examples.




This example contains content which pertains directly to this week’s assignment. It demonstrates how to alter styles or text on a web page using JS.




<strong>Example 1: </strong><u>https://www.albany.edu/~cv762525/cinf201/examples/page-output-example.html</u>




This link contains examples of previously discussed concepts from Week 9 in addition to examples from this week’s content.




<strong>Example 2: </strong><u>https://www.albany.edu/~cv762525/cinf201/examples/js-concepts-example-2.html</u>




<h1>JS Challenges 2 (CW/HW)</h1>

Download the “JS-Challenges-2.zip” folder from Blackboard under today’s Lecture Notes or the Assignment folder. Extract everything from inside of this zip folder to some place where you will be able to find them easily. Inside of the zip folder will be an HTML file and an MP4 file (video) which will explain how the assignment should work and where to begin.




Your task is to read the challenges displayed on the HTML page and add JS as needed to complete them. Underneath each challenge description is a set of &lt;script&gt;&lt;/script&gt; tags where you will place your JavaScript.




<u>Review the two examples from this week (listed above) as they both contain code that can be</u> <u>used for these challenges.</u>




To view all other class examples, visit this link and click whatever you want to see. The js folder contains the various JS files used for the examples.




<u>https://www.albany.edu/~cv762525/cinf201/examples/</u>


