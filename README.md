##Command Line Basics

What are the terminal commands to:

* Create a new folder called "Blah"

```
mkdir Blah
```
* Move into the newly created "Blah" folder

```
cd Blah
```
* Create a "hello.rb" file

```
touch hello.rb
```

* Open the "hello.rb" file in Sublime Text

```
subl hello.rb
```

* Move back one directory

```
cd ..
```

*** 

##HTML and CSS

* Without looking it up, create the basic HTML template structure with `Doctype`, `head`, `title`, and `body`

```
<!doctype html>
<html>
<head><title>Something</title></head>
<body>
</body>
</html>
```

* Write the HTML to add a link to google.com

```
<a href="http://www.google.com">Google Link</a>

```

* Link to an external sheet at the path "css/styles.css"

```
...
<head>
<link rel="stylesheet" href="/css/styles.css">
</head>
...
```

* Why do we want to use external stylesheets and scripts instead of adding them directly into our HTML file?

```
Separation of Concerns
```

* What's the difference between a class and an ID?  Why do we use them?

```
id = used once
class = used many times

```

Using the following HTML: 

```
	<h1>Hello Guys!</h1>
	<p>Don't Mess This Quiz Up!!!</p>
	<div>
	  <p>I'm a paragraph!</p>
	  <p class="lol">I have a class!</p>
	  <p id="wdi">I have an ID!</p>
	</div>

```

* Write CSS to change the color of the `<h1>`

```
h1 {
  color: blue;
}
```

* Write CSS to give the `<p>` with the id of 'wdi' a different font size

```
	p#wdi{
		font-size: 30px;
	}
	
	#wdi {
	}
	
```

* Write CSS to give the `<p>` with the class of 'lol' a background color.

```
//all class .lol
.lol {
  background: blue;
}

//p inside of lol
.lol p {
  background: blue;
}

//p with class lol
p.lol {
}

```

* Write CSS to give the first `<p>` in the `<div>` a yellow border.

```
div > p:first-child {
	border: 5px solid yellow;
}

div p:nth-child(1) {
}

```

* Name at least two of the different color formats used in CSS

```
hex
rgb
rgb/a
hsl
```

***

##Ruby

* What are the different data types in Ruby?

```
booleans, numbers (integers/floats/fixnum), strings, symbols, arrays/hashes
```

* How do you print something to the terminal in Ruby?

```
puts "something"
p "something"

```

* What is an array?

```
Sequentially/Indexed
collection of data, storing many types
```

* Create an array with 5 of your favorite foods

```
foods = ["quesidilla", "pizza", "tacos", "kale", "burrito"]
```

* Write code to print out the numbers from 1 to 250

```
250.times {|x| puts x}

1.upto(250) {|x| puts x}

count = 1
while (count <= 250) do
 puts count
 count += 1
end

```

***

#Javascript

* Aside from syntax, how is Javascript different from Ruby? 

```
* JavaScript can run in the browser and on the server (with NodeJS), while Ruby runs only on the server.
* JavaScript is asynchronous, while Ruby is synchronous.
* Ruby has symbols, while JavaScript does not.
* Ruby has different number types (Integer, Float, Bignum, Fixnum), while JavaScript only has Number (which is a float / decimal point number)
... just to name a few
```

* How do you print something to the console in Javascript?

```
console.log("hi")
```

* Using a for loop, write code to print out all the odd numbers between 1 and 100.  You will also need to use an if statement.

```
for (var i = 0; i <= 100; i++) {
  if (i % 2 !== 0) {
    console.log(i);
  }
}
```

***

##Git

* What is Git?  What is Github?

```
Git is the version control program we will be using to store our code.  Github is a website that you can store a copy of your code on and allows for easy collaboration with others.
```

* What is the command to create an empty git repository in terminal?

```
git init
```

* What is the difference between `git add` and `git commit`?

```
git commit saves the files.  Before you can call git commit, you need to call git add in some fashion to stage the files that will be committed.  If you call git commit before you've added anything, then nothing will be committed!
```

***


##Optional Bonus

If you finish early, work on this problem:

Using either Ruby or Javascript, write code that will test if a given string is a palindrome.  A palindrome is a word that is the same forwards and backwards, like 'mom' or 'racecar' or 'aibohphobia'.  You are not allowed to use the built in `reverse` method or any similar methods.

```
Below is one solution we worked on in class.  There were many ways to solve this though!

var word = "pizza";//"racecar";
var arr = word.split("");
var copy = [];
for (var i = 0; i < arr.length; i += 1) {
  copy.unshift(arr[i]);
}
var one = arr.join("");
var two = copy.join("");
var isPalindrome = one == two;
console.log("one", one);
console.log("two", two);
console.log("isPalindrome", isPalindrome);
```





