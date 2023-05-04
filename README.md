Download Link: https://assignmentchef.com/product/solved-cs60007-assignment3-convex-hull-dandc
<br>



<ol>

 <li>All codes should be written in C/C++ that can be compiled using GNUcompiler and run in Ubuntu.</li>

 <li>Don’t copy codes from other groups. It is subject to penalty or failing in theextreme case.</li>

 <li>All group members should participate in coding and with uniform division oftasks. In vivas, we may ask each individual to modify codes so as to change something or the other.</li>

 <li>How to write an svg file?</li>

</ol>

Just download and save <a href="http://cse.iitkgp.ac.in/~pb/test.svg">http://cse.iitkgp.ac.in/</a><a href="http://cse.iitkgp.ac.in/~pb/test.svg">~</a><a href="http://cse.iitkgp.ac.in/~pb/test.svg">pb/test.svg</a><a href="http://cse.iitkgp.ac.in/~pb/test.svg">.</a> Open it in a browser, and also open it a plain text editor. Compare the image with the text—you will understand the basics. It’s very simple.

There are many resources on svg file format available in Internet. The most important one is <a href="https://www.w3schools.com/svg/">http://www.w3schools.com/svg/</a> where you will find many examples.

A properly written svg can always be opened and seen in any browser like Mozilla or Chrome, and also in any standard image viewer. So, just check and ensure that the output svg produced by your code is opened and seen properly in these two browsers.

<ol start="5">

 <li>Use proper indentation and commenting in your codes so that we can understand your code.</li>

 <li>Write in the beginning of each code the following:

  <ol>

   <li>your names and roll nos.</li>

   <li>purpose of the code / problem description in briefiii) compilation and execution instructions in Ubuntu iv) any other point that you feel important.</li>

  </ol></li>

 <li>You have to submit all source codes and 3 sets of input and output files (small,medium, and large sizes).</li>

</ol>

<h1>1           Convex hull (divide and conquer)</h1>

<ol start="20">

 <li>Write a program to randomly generate <em>n </em>distinct points such that their coordinates are integers in the range [20<em>,</em>800] and divisible by 20. User input: <em>n</em>.</li>

</ol>

Store the value of <em>n </em>and the coordinates of all <em>n </em>points in a plain text file named points.txt.

<ol>

 <li>Write another program that reads the file txt and constructs its convex hull using divide and conquer.</li>

</ol>

Visualize the left convex hull in red and the right one in blue.

For the left convex hull, find the convex hulls of the points lying in its interior, and visualize them as above.

For the right one, do similar.

So, finally, hierarchical convex hulls will be formed.

Save the final result as an svg file named hull.svg in which all <em>n </em>points are colored black and hull edges colored red / blue.

<h1>2           Convex hull (Graham scan)</h1>

<ol start="20">

 <li>Write a program to randomly generate <em>n </em>distinct points such that their coordinates are integers in the range [20<em>,</em>800] and divisible by 20. User input: <em>n</em>.</li>

</ol>

Store the value of <em>n </em>and the coordinates of all <em>n </em>points in a plain text file named points.txt.

<ol>

 <li>Write another program that reads the file txt and constructs its convex hull using Graham scan. Visualize the convex hull <em>H</em><sub>1 </sub>in red.</li>

</ol>

Next, find the convex hull <em>H</em><sub>2 </sub>of the points lying in the interior of <em>H</em><sub>1</sub>, and visualize it in blue.

This way, hierarchical convex hulls will be formed.

Save the final result as an svg file named hull.svg in which all <em>n </em>points are colored black and hulls are colored alternately in red and blue.

<h1>3           Euclidean MST by Prim’s Algorithm</h1>

The task is to find MST by Prim’s Algorithm for a completely connected Euclidean graph. (For an Euclidean graph, the weight of each edge is given by the Euclidean distance between its two endpoints.) User input: integers <em>k,n</em><sub>1</sub><em>,n</em><sub>2</sub><em>,n</em><sub>3</sub>.

<ol>

 <li>a) Write a program that takes as input the centers and the radii of three circles as follows:</li>

</ol>

1st circle: center = (125<em>,</em>175)<em>,r</em><sub>1 </sub>= 100 + ∆

2nd circle: center = (300<em>,</em>175)<em>,r</em><sub>2 </sub>= 150 + ∆ 3rd circle: center = (175<em>,</em>325)<em>,r</em><sub>3 </sub>= 125 + ∆ where ∆ is a random integer in the interval [−<em>k,k</em>], <em>k </em>= user input.

Now, generate points on these circles as follows. They will serve as the vertices of the graph.

Generate the intersection points of the circles.

In addition, for each circle, generate random points lying on the circle so that two consecutive points are neither “too close” nor “too far”.

The number of points <em>n</em><sub>1</sub><em>,n</em><sub>2</sub><em>,n</em><sub>3 </sub>on the three circles should be taken as input during execution of your code.

<ol>

 <li>Consider the completely connected Euclidean graph defined by the above set ofvertices, and compute its MST using Prim’s algorithm.</li>

 <li>Save the input and the output as svg and out.svg, as shown in the figure.</li>

</ol>

Output: MST.

on which they lie. Edges are not shown for clarity.

<h1>4           Dijkstra’s algorithm on Euclidean graph</h1>

The task is to find single-source shortest paths for a directed Euclidean graph. (For an Euclidean graph, the weight of each edge is given by the Euclidean distance between its two endpoints.) User input: integers <em>k,c,r,n</em><sub>1</sub><em>,n</em><sub>2</sub>.

<ol>

 <li>Write a program that draws <em>k </em>circles with center <em>c </em>and radii <em>r<sub>i </sub></em>= <em>ri </em>for <em>i </em>=</li>

</ol>

1<em>,</em>2<em>,…,k</em>.

Now, randomly generate points on these circles so that the number of points on the <em>i</em>-th circle lies between <em>n</em><sub>1</sub>√<em>r<sub>i </sub></em>and <em>n</em><sub>2</sub>√<em>r<sub>i</sub></em>. These points will serve as the vertices of the graph. Care should be taken so that for each circle, two consecutive points are neither “too close” nor “too far”.

<ol>

 <li>For <em>i </em>= 1<em>,</em>2<em>,…,k</em>, let <em>P<sub>i </sub></em>denote the set of random points on the <em>i</em>-th circle. Consider the directed Euclidean graph <em>G</em>(<em>V,E</em>), where</li>

</ol>

and <em>.</em>

Compute shortest paths from <em>c </em>to all vertices.

<ol>

 <li>Save the input and the output as dijk-in.svg and dijk-out.svg, as shown in the figure.</li>

</ol>

Input graph (<em>k </em>= 4). Vertices are random points on the concentric

Output: Shortest paths from <em>c</em>.

circles, edges are not shown for clarity.

<h1>5           <em>s</em>–<em>t </em>shortest path</h1>

The task if to find a shortest path from a source <em>s </em>to a destination <em>t </em>in an Euclidean graph. (For an Euclidean graph, the weight of each edge is given by the Euclidean distance between its two endpoints.) User input: integers <em>k,m,n,g</em>.

<ol>

 <li>Write a program that randomly generates <em>k </em>unit squares in a grid of size <em>m </em>× <em>n </em>with <em>g </em>as the grid unit.</li>

</ol>

The corners of the squares should coincide with the grid points. The squares are basically obstacles.

The grid points are the vertices of the graph <em>G</em>(<em>V,E</em>). (<em>p,q</em>) is an edge of the graph if and only if the straight line segment <em><span style="text-decoration: line-through;">pq </span></em>does not intersect the interior of any square.

Compute a shortest path, if any, from <em>s </em>to <em>t</em>, where <em>s </em>is the bottom-left grid point, and <em>t </em>the top-right one.

<ol>

 <li>Save the output as svg, as shown in the figure.</li>

</ol>

<em>k </em>= 8                                                                                                                                      <em>k </em>= 10

<em>L </em>= 1+2√13 ≈ 8<em>.</em>211                                                                                            <em>L </em>= 1+√2+√5+√13 ≈ 8<em>.</em>256

<h1>6           Tiling</h1>

Omino means a unit square, whereas domino means two ominoes, i.e., a rectangle of size 1 × 2 or 2 × 1.

A polyomino or <em>n</em>-omino is basically an axis-parallel polygon comprising <em>n </em>ominoes. Given an <em>n</em>-omino, the task is to represent it as the smallest collection of dominoes and ominoes.

User input: integers <em>m,n</em>(<em>n </em>≤ <em>m</em><sup>2</sup>).

Use the following steps for coding:

<ol>

 <li>Generate a random <em>n</em>-omino in a square <em>S </em>of size <em>m </em>× <em>m </em> The size of an omino may be 15 × 15 or so, and its center should be marked by a dot.</li>

</ol>

You can place the first omino at the left-bottom place of <em>S</em>, and then place each new omino at some random place inside <em>S </em>so that the new omino shares an edge with an existing omino.

Iterate until you get <em>n </em>ominoes.

In figure (a), <em>n </em>= 23, and the ominoes are numbered in the order as generated.

<ol>

 <li>Use maximum matching in a bipartite graph to find the maximum number ofdominoes that can cover the <em>n</em>-omino as much as possible. Color the dominoes and the leftover ominoes as shown in figure (c).</li>

</ol>

The graph <em>G</em>(<em>V,E</em>) has <em>V </em>= {ominoes} and <em>E </em>= {(<em>u,v</em>) : omnio <em>u </em>and omino <em>v </em>have a common edge}.

Since this is a subgraph of a graph representing a chequer-board, it is 2-colorable and hence bipartite.

<ol>

 <li>Save the input <em>n</em>-omino as svg, polyomino2.svg, and the output</li>

</ol>

as tiling.svg, as shown in figures (a–c).

<table width="469">

 <tbody>

  <tr>

   <td rowspan="2" width="21"></td>

   <td colspan="5" width="107"><em>S</em></td>

   <td rowspan="6" width="43"> </td>

   <td width="21"></td>

   <td colspan="6" width="149"> </td>

   <td rowspan="2" width="21"></td>

   <td colspan="5" width="107"> </td>

  </tr>

  <tr>

   <td width="21">16</td>

   <td width="21">23</td>

   <td colspan="3" width="64"> </td>

   <td width="21"></td>

   <td width="21"></td>

   <td width="21"></td>

   <td colspan="4" width="107"> </td>

   <td colspan="2" width="43"></td>

   <td colspan="3" width="64"> </td>

  </tr>

  <tr>

   <td width="21"> </td>

   <td width="21">13</td>

   <td width="21">14</td>

   <td width="21">11</td>

   <td width="21">19</td>

   <td rowspan="3" width="21">15</td>

   <td width="21"> </td>

   <td width="21"></td>

   <td width="21"></td>

   <td width="21"></td>

   <td width="21"></td>

   <td colspan="3" width="85"> </td>

   <td colspan="2" width="43"></td>

   <td rowspan="2" width="21"></td>

   <td rowspan="2" width="21"></td>

   <td rowspan="2" width="21"> </td>

  </tr>

  <tr>

   <td width="21">4</td>

   <td rowspan="2" width="21">5</td>

   <td width="21">6</td>

   <td width="21">9</td>

   <td width="21">17</td>

   <td width="21"></td>

   <td width="21"></td>

   <td width="21"></td>

   <td width="21"></td>

   <td width="21"></td>

   <td colspan="2" width="64"> </td>

   <td width="21"></td>

   <td rowspan="2" width="21"></td>

   <td rowspan="2" width="21"></td>

  </tr>

  <tr>

   <td rowspan="2" width="21"> </td>

   <td width="21"> </td>

   <td width="21">8</td>

   <td width="21">10</td>

   <td width="21"></td>

   <td width="21"></td>

   <td width="21"></td>

   <td width="21"></td>

   <td width="21"></td>

   <td width="21"></td>

   <td rowspan="2" width="43"> </td>

   <td rowspan="2" width="21"></td>

   <td colspan="2" width="43"></td>

   <td width="21"></td>

  </tr>

  <tr>

   <td width="21"> </td>

   <td width="21"> </td>

   <td width="21"> </td>

   <td width="21">12</td>

   <td width="21">20</td>

   <td width="21"></td>

   <td width="21"> </td>

   <td width="21"></td>

   <td width="21"> </td>

   <td width="21"></td>

   <td width="21"></td>

   <td width="21"> </td>

   <td width="21"></td>

   <td width="21"> </td>

   <td colspan="2" width="43"></td>

  </tr>

 </tbody>

</table>

a                                         b                                         c

<h1>7           Maximum line matching</h1>

<ol>

 <li>Write a program to randomly generate <em>m </em>horizontal straight line segments and <em>n </em>vertical straight line segments with the following constraints:

  <ol start="800">

   <li>The endpoints should be random integers in multiples of 20 and should lieinside a rectangle <em>R </em>of width 1000 and height 800.</li>

   <li>The endpoints of each segment should be distinct, i.e., each segment shouldhave positive length.</li>

  </ol></li>

</ol>

<ul>

 <li>Two horizontal segments should not overlap or share an endpoint.iv) Two vertical segments should not overlap or share an endpoint.</li>

</ul>

<ol>

 <li>v) A horizontal segment and a vertical segment should not share an endpoint.</li>

</ol>

Store the values of <em>m,n</em>, and the coordinates of all endpoints in a meaningful order in a txt file named hvLines.txt.

User input: <em>m</em>, <em>n</em>.

<ol>

 <li>Write another program that reads the file txt, computes the intersection among the line segments, find the maximum matching in which each pair comprises a horizontal and a vertical segment. Save the final result as an svg file named pairs.svg, with a diamond centered at the intersection point of each pair, and showing the unmatched segments as dashed.</li>

</ol>

input                                                      output

line segments can intersect at interior points only

<h1>8           2-color intersection</h1>

<ol>

 <li>Write a program to randomly generate <em>m </em>horizontal straight line segments and <em>n </em>vertical straight line segments with the following constraints:

  <ol>

   <li>The endpoint coordinates should be random integers in multiples of 20 andshould lie in [20<em>,</em>1000].</li>

   <li>The length of each segment should be 80.iii) Two horizontal segments should not overlap or share an endpoint. iv) Two vertical segments should not overlap or share an endpoint.</li>

   <li>v) A horizontal segment and a vertical segment should not share an endpoint. vi) An intersection point cannot be any endpoint.</li>

  </ol></li>

</ol>

Store the values of <em>m,n</em>, and the coordinates of all endpoints in a meaningful order in a txt file named hvLines.txt.

User input: <em>m</em>, <em>n</em>.

<ol>

 <li>Write another program that reads the file txt, computes the intersection among the line segments, and color the intersection points and endpoints using two colors (red and blue) such that no two consecutive points on the same segment get the same color.</li>

</ol>

Save the final result as an svg file named intersect.svg.

input                                                      output