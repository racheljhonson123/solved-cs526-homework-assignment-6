Download Link: https://assignmentchef.com/product/solved-cs526-homework-assignment-6
<br>
The goal of this assignment is to give students an opportunity to compare and observe how running times of sorting algorithms grow as the input size (which is the number of elements to be sorted) grows. Since it is not possible to measure an accurate running time of an algorithm, you will use an <em>elapsed time</em> as an approximation. How to calculate the elapsed time of an algorithm is described later.




You will use four sorting algorithms for this experiment: insertion-sort, merge-sort, quick-sort and heap-sort. A code of insertion-sort is in page 111 of our textbook. An array-based implementation of merge-sort is shown in pages 537 and 538 of our textbook. An array-based implementation of quick-sort is in page 553 of our textbook. You can use these codes, with some modification if needed, for this assignment. For heap-sort, our textbook does not have a code. You can implement it yourself or you may use any implementation you can find on the internet or any code written by someone else. If you use any material (pseudocode or implementation) that is not written by yourself, you must clearly show the source of the material in your report.




A high-level pseudocode is given below:




for <em>n</em> = 10,000, 20,000, . . ., 100,000 (for ten different sizes)

Create an array of <em>n</em> random integers between 1 and 1,000,000 Run <strong>insertionsort</strong> and calculate the elapsed time // make sure you use the initial, unsorted array Run <strong>mergesort</strong> and calculate the elapsed time

// make sure you use the initial, unsorted array

Run <strong>quicksort</strong> and calculate the elapsed time

// make sure you use the initial, unsorted array

Run <strong>heapsort</strong> and calculate the elapsed time




You can generate <em>n</em> random integers between 1 and 1,000,000 in the following way:




Random r = new Random( );  for <em>i</em> = 1 to <em>n </em>

a[i] = r.nextInt(1000000) + 1




You can also use the <em>Math.random</em>( ) method. Refer to a Java tutorial or reference manual on how to use this method.




Note that it is important that you use the initial, unsorted array for each sorting algorithm. So, you may want to keep the original array and use a copy when you run each sorting algorithm.




You can calculate the elapsed time of the execution of a sorting algorithm in the following way:




long startTime = System.currentTimeMillis(); call a sorting algorithm

long endTime = System.currentTimeMillis();

long elapsedTime = endTime ‐ startTime;







Collect all elapsed times and show the result (1) as a table and (2) as a line graph.




The table should look like:




<table width="623">

 <tbody>

  <tr>

   <td width="80">        <em>n</em><em>Algorithm </em></td>

   <td width="54">10000</td>

   <td width="54">20000</td>

   <td width="54">30000</td>

   <td width="54">40000</td>

   <td width="54">50000</td>

   <td width="54">60000</td>

   <td width="54">70000</td>

   <td width="54">80000</td>

   <td width="54">90000</td>

   <td width="58">100000</td>

  </tr>

  <tr>

   <td width="80">insertion</td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="58"> </td>

  </tr>

  <tr>

   <td width="80">merge</td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="58"> </td>

  </tr>

  <tr>

   <td width="80">quick</td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="58"> </td>

  </tr>

  <tr>

   <td width="80">heapsort</td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="54"> </td>

   <td width="58"> </td>

  </tr>

 </tbody>

</table>




Entries in the table are elapsed times in milliseconds.




The line graph shows the same information but as a graph with four lines, one for each sorting algorithm. The <em>x</em>-axis of the graph is the input size <em>n</em> and the <em>y</em>-axis of the graph is the elapsed time in milliseconds. The following is an example graph:


