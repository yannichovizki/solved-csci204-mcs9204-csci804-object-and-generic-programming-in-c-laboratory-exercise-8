Download Link: https://assignmentchef.com/product/solved-csci204-mcs9204-csci804-object-and-generic-programming-in-c-laboratory-exercise-8
<br>
<strong>Task One: I/O Manipulators (0.3 marks) </strong>

Define a manipulator <em>format</em> in a file <strong>task1.cpp</strong>. The manipulator <em>format</em> can take three arguments: string of base (such as “oct”, “dec” and “hex”), the length that an integer can be displayed, and a character can be used to pad the output value when the length of the value is not long enough. Write a driver program include main() function in the file <strong>task1.cpp</strong> to test the manipular. For example:        cout &lt;&lt; format(“oct”, 10, ‘#’) &lt;&lt; 20 &lt;&lt; endl;

The result is

########24

Change the format like

cout &lt;&lt; format(“hex”, 8, ‘!’) &lt;&lt; 20 &lt;&lt; endl;

The result is

!!!!!!14

Change the format like

cout &lt;&lt; format(“dec”, 12, ‘@’) &lt;&lt; 20 &lt;&lt; endl;

The result is

@@@@@@@@@@20

<strong> </strong>

<strong>Task Two: A PGM Reader (0.7 Marks) </strong>

In this task, you are required to develop a program, <strong>pgmReader</strong>, to read a gray-scale image saved in pgm format (<strong>PGM</strong>, Portable Gray Map). The task should be completed in two steps:

<ul>

 <li>Design and implementation of class Image as described below.</li>

 <li>Design and implement the program, <strong>pgmReader, </strong>as specified below<strong>.</strong></li>

</ul>




An image consists of a grid of pixels (picture elements). For a gray-scale image, each pixel has one value representing its luminance or brightness.  The pixel value usually ranges from 0 to 255, with 0 being the darkest (black) and 255 being the brightest (white).




<strong>PGM</strong> is a simple file format to store gray-scale images. You are required to design and develop a class, <strong>Image</strong>, that is able to read a gray scale image from a PGM image file and report the following

statistics of the image: width, height, minimum intensity, maximum intensity, and average intensity. You are required to declare the <strong>Image</strong> class in <strong>Image.h</strong> and place its implementation in <strong>Image.cpp. </strong>Read the appendix for the specifications of PGM.

<strong> </strong>

Using the <strong>Image</strong> class, design and implemented a main program, <strong>pgmReader.cpp, </strong>that reads an image stored in a PGM format file, calculates and outputs the statistics. Following are examples that show how your program may be used and marked. Note: <strong>$</strong> is assumed to be the prompt of a UNIX terminal.




$ pgmReader c01.ppm

&lt;c01.ppm&gt; is not a PGM file




$ pgmReader c01.pgm

Read a gray-scale image from a PGM file &lt;c01.pgm&gt;.

Statistics of the image:

Width:         1024

Height:        768

Min-Intensity: 0 Max-Intensity: 255

Ave-Intensity: 131.95




The compile directive would be something like




g++ –o pgmReader pgmReader.cpp Image.cpp







Two PGM images are provided for testing your program.