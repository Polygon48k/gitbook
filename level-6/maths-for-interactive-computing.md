# Maths for Interactive Computing

## Maths for Interactive Computing <a id="maths-for-interactive-computing"></a>

[Specification](https://lecturerscott.files.wordpress.com/2017/12/fn84-11-unit-specification.pdf)

[Practice Test](https://goo.gl/forms/qqjltWsiuivGE0qk2)

## Number Sets <a id="number-sets"></a>

Number Sets are categories of number types

#### Natural <a id="natural"></a>

Positive Integers \(whole numbers\)  
1, 2, 3, 4, 5 etc.

#### Integer <a id="integer"></a>

This includes Natural numbers and their negatives

-5, -4, -3, -2, -1, 0, 1, 2, 3, 4, 5

#### Rational <a id="rational"></a>

Rational numbers are the ratios of integers, also called fractions, such as 1/2 = 0.5 or 1/3 = 0.333…

#### Real <a id="real"></a>

Real numbers include non-whole numbers, for example, 2.13, 8.4656, 9,102.3

Real numbers include transcendental numbers, that is, numbers with infinite description, such as pi

## Decimal to Binary <a id="decimal-to-binary"></a>

Everything inside computers is made up of binary. Binary just means one of two. This can be True or False. Yes or No, On or Off. 1 or 0.

We need to know how to figure out what some numbers are in binary and turn them into normal numbers that normal people use. \(and the other way round\).

This is 8 bit binary btw, It’s the only type you have to worry about. It means the biggest number you will be asked about is 255. Anything else is probably a trick question :S

So, 25 in binary is 11001

Why?

Don’t know, but I’ll show you how to figure it out tl:dr…

So, you basically take your number

25

divide it in two

12.5 and dingy the .whatever so 12

divide it in two

6

divide it in two

3

divide it in two

1.5, dingy the .whatever again, so 1

so we have 1, 3, 6, 12, 25

For each number now we see if it is odd or even, odd gets 1, even gets 0, so…

1 1 0 0 1

Bosh, we got our answer, and we don’t even know what’s going on!

Done!

## Hexidecimal to Decimal <a id="hexidecimal-to-decimal"></a>

![enter image description here](http://schoolcoders.com/w/images/1/13/Hex-table.png)

When taking a Hexadecimal number, for three figure numbers, we use the equation

\(Character1 \* 256\) + \(Character2 \* 16\) + \(Charater3\)

For Example

6FF = \(6 \* 256\) + \(15 \* 16\) + \(15\)

or 1,536 + 240 + 15 = 1,791

This equation is a simplified version of

[![h\_{n}16{n}+h\_{n-1}16{n-1}+\cdots +h\_{1}16{1}+h\_{0}16{0}](https://cdn.sparkfun.com/assets/learn_tutorials/2/1/0/hex_positional-notation-02.png)](https://cdn.sparkfun.com/assets/learn_tutorials/2/1/0/hex_positional-notation-02.png)

Where you can substitute 16 for which ever base you with to use.

## Interior Angles <a id="interior-angles"></a>

![enter image description here](https://upload.wikimedia.org/wikipedia/commons/thumb/e/eb/Regular_polygon_3_annotated.svg/1200px-Regular_polygon_3_annotated.svg.png)

Interior Angles of a triangle will all add up to 180 Degrees.

For most simple shapes we can break them down into multiple triangles.

![Regular Pentagon](https://www.mathsisfun.com/geometry/images/interior-angles-pentagon.gif)

By using this method we can ascertain the interior angles of simple 2D shapes.

a + b + c = 180°

To find the total interior angle of a shape we can use the equation \( n- 2 \) 180°, where n is the number of sides

## Areas and Perimeters <a id="areas-and-perimeters"></a>

The area of regular four side shapes can be calculated by multiplying the length and height together.

![enter image description here](https://www.mathsisfun.com/geometry/images/area/rectangle.gif)

2 x 4 = 8²

The area of a circle can be calculated using πr²

π \( pi \) can is an infinite number but can be rounded off to two decimal places for these calculations, 3.14

Where r is the radius.  
![Circle](https://www.onlinemathlearning.com/image-files/xarea-circle.png.pagespeed.ic.pHsq7ZnD4v.png)

π2² = 12.57

## Volumes and Surface Area <a id="volumes-and-surface-area"></a>

The surface area of a cube can be calculated by multiplying the area by the depth

4² x 2 = 8³

## Vectors <a id="vectors"></a>

A **vector** describes a movement from one point to another. A vector quantity has both direction and magnitude \(size\).

![Graphics Representation of a Vector](https://bam.files.bbci.co.uk/bam/live/content/zqc7xnb/small)

The Vector below, represents move across 3 units to the right, and, then down by 2 units

![enter image description here](https://equation-chef.files.bbci.co.uk/content/483c7077bbcd16ace3b0f9f8adea2ffb/18)

![enter image description here](https://bam.files.bbci.co.uk/bam/live/content/zpqnyrd/small)

When we multiply a a vector by a scalar, we simply multiply each number

![enter image description here](https://equation-chef.files.bbci.co.uk/content/8202968ce49ef74ace35762a2342e9b0/18)

## Simplifying Equations <a id="simplifying-equations"></a>

BODMAS is a useful acronym that lets you know which order to solve mathematical problems.

The **BODMAS** acronym is for:

* **B**rackets \(parts of a calculation inside brackets always come first\).
* **O**rders \(numbers involving powers or square roots\).
* **D**ivision.
* **M**ultiplication.
* **A**ddition.
* **S**ubtraction.

## Random Number Generators <a id="random-number-generators"></a>

Random number generators are usually called with a function RND  
In order to receive an expected output we need to define the seed value.  
The see value defines the maximum number output from the random number generator.  
It is common to manipulate Random Number Generators to conform to human expectation, as, we commonly reject or see patterns in truly random sequences. ie, we may see a single number repeated

## Expressing negative Indicies <a id="expressing-negative-indicies"></a>

Indicies are practically powers of  
We can express negative powers in order to generate a negative output. This can also be a more efficient way to store negative numbers.

## Flow Charts <a id="flow-charts"></a>

Flow charts express how the logic of a sequence of events plays out. By using the below key we can express this graphically, allowing us to plan events before programming.

![enter image description here](https://www.smartdraw.com/flowchart/img/basic-symbols.jpg?bn=1510011142)

[flow.io](http://flow.io/)

