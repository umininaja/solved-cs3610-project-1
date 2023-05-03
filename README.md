Download Link: https://assignmentchef.com/product/solved-cs3610-project-1
<br>
A prime number is a number greater than 1 that has no positive integer divisors other than 1 and itself. Conversely, a composite number is any number greater than 1 that is divisible by numbers other than 1 and itself. In other words, a composite number is any number greater than 1 that is not a prime number. To help elucidate the distinction between these two types of numbers, you will write a program that accepts as input a positive integer <em>n </em>and outputs a list of all the prime numbers in the range [2<em>,n</em>] followed by a list of all the composite numbers lying in the same range. To ensure that your program always terminates within a reasonable amount of time, you will separate the prime and composite numbers using the Sieve of Eratosthenes.

The Sieve of Eratosthenes is an algorithm designed to efficiently find all prime numbers less than a given integer limit <em>n</em>. The algorithm indirectly identifies prime numbers by iteratively marking as composite the multiples of each prime found starting from the first prime number 2. The steps of the algorithm are enumerated as follows:

<ol>

 <li>Create an ordered list <em>l </em>of all integers in the range [2<em>,n</em>].</li>

 <li>Initialize the first prime number <em>p </em>= 2.</li>

 <li>Starting from index 2 ∗ <em>p</em>, iterate over the ordered list <em>l </em>in increments of <em>p </em>and place a mark on each number visited.</li>

 <li>Find the first unmarked number larger than <em>p </em>in the ordered list <em>l</em>. If no such number is found, exit the algorithm, otherwise, set <em>p </em>to the unmarked value.</li>

</ol>

√

<ol start="5">

 <li>If <em>p &gt; </em>b <em>n</em>c, exit the algorithm, otherwise, return to step 3. b<em>…</em>c is the floor function (<a href="https://en.wikipedia.org/wiki/Floor_and_ceiling_functions">https://en.wikipedia.org/wiki/Floor_and_ceiling_functions</a><a href="https://en.wikipedia.org/wiki/Floor_and_ceiling_functions">)</a></li>

</ol>

An illustrative example of the Sieve of Eratosthenes is provided as follows:

<ul>

 <li><em>n </em>= 10</li>

</ul>

<em>l </em>= [2<em>,</em>3<em>,</em>4<em>,</em><a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a><em>,</em>6<em>,</em>7<em>,</em>8<em>,</em>9<em>,</em>10].

<ul>

 <li>1st Iteration:

  <ul>

   <li>= 2 (First prime number) Iterate and mark in increments of 2.</li>

  </ul></li>

 <li>2nd Iteration:

  <ul>

   <li>= 3 (Next unmarked number larger than 2)Iterate and mark in increments of 3.</li>

  </ul></li>

 <li>3rd Iteration: p = 5√</li>

</ul>

1

<ul>

 <li>Final Result:</li>

</ul>

Prime: [2<em>,</em>3<em>,</em>5<em>,</em>7] Composite: [

<h1>Input</h1>

A single command line argument containing a positive integer <em>n </em>with the constraints

2 ≤ <em>n </em>≤ 30000

<h1>Output</h1>

Using space as a delimiter, print all prime numbers less than or equal to <em>n </em>on one line followed by all composite numbers less than or equal to <em>n </em>on a separate line. If the value of <em>n </em>does not lie in the constrained range [2<em>,</em>30000], output the message Out of range. If <em>n </em>is not an integer, output the message Nan. If <em>n </em>is not provided as input, output the message Missing argument.

<h1>Sample Test Cases</h1>

<strong>Test Case 1</strong>

$ ./a.out 10

2 3 5 7

4 6 8 9 10

<strong>Test Case 2</strong>

$ ./a.out

Missing argument

<a href="#_ftnref1" name="_ftn1">[1]</a> <em>&gt; </em>b 10c so exit algorithm.