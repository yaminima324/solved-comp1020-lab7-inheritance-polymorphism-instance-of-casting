Download Link: https://assignmentchef.com/product/solved-comp1020-lab7-inheritance-polymorphism-instance-of-casting
<br>
<ul>

 <li>Inheritance, polymorphism, instanceof, casting</li>

</ul>

Notes:

<ul>

 <li>The three exercises are cumulative – each builds on the previous one.</li>

 <li>Only one of the three exercises is required.</li>

 <li>Try to complete the Bronze and Silver exercises. The Gold exercise is trickier, as usual.</li>

</ul>

<h1>Creating a class hierarchy</h1>

<ol>

 <li>Create three classes <strong>Data</strong>, <strong>Single</strong>, and <strong>List</strong>, as follows:

  <ol>

   <li>Create an <strong><em>abstract</em></strong> class <strong><sub>Data</sub></strong>, which will contain no instance variables, no constructor, and only one method: <strong>double valueOf()</strong> which returns <strong>0</strong>.</li>

   <li>Create a class <strong>Single</strong> which is a subclass of <strong>Data</strong>, and which will store one <strong>double</strong> Provide a constructor to initialize the value. Override the <strong>valueOf()</strong> method so that it returns this value.</li>

   <li>Create a class <strong>List</strong> which is a subclass of <strong>Data</strong>, and which will store a <strong>double[]</strong> Provide a constructor <strong>List(double[] a)</strong> which will initialize this array. Override the <strong>valueOf()</strong> method so that it returns the <strong><em>sum</em></strong> of all the <strong>double</strong>s in the array. Note that this will always be a <em>full</em> array, not a <em>partially full</em> array. There will be <em>no</em> separate length variable.</li>

  </ol></li>

 <li>Start with the <strong>java</strong> file. It creates a list of <strong>Data</strong> objects (a mixture of <strong>Single</strong> and <strong>List</strong>) using a <strong>Data[] myData</strong> array. Take a look at it. Add a loop at the indicated position which will find and print the sum of every number that appears in <strong><sub>myData</sub></strong>, whether it appears in a <strong>Single</strong> or in a <strong>List</strong>, using <strong>valueOf()</strong>. It should print the line</li>

</ol>

<strong>The sum of everything is 35.8</strong>




<ol>

 <li>Add a <strong>length()</strong> method to the <strong>List</strong> class which returns the size of the list stored in the object.</li>

</ol>

You are <strong><em>not</em></strong> allowed to add a <strong>length()</strong> method to the <strong>Data</strong> or <strong>Single</strong> classes. (This would be a logical thing to do, but it would destroy the purpose of the question.)

<ol start="2">

 <li>Add more code to the <strong>java</strong> file at the indicated position which will find and print the total number of values that appear anywhere in <strong>myData</strong>. It should print the line <strong>There are 7 values in total.</strong> as well as the output line from the Bronze exercise.</li>

</ol>







<ol>

 <li>Look at the file <strong>java</strong>. Note that the <strong>Data[]</strong> array has been replaced by an <strong>Object[]</strong> array instead. This <strong>Object </strong>array contains <strong>Single </strong>and <strong>List </strong>objects, but it also contains <strong>String</strong>s and other types as well.</li>

 <li>Paste your code from the Bronze and Silver exercises into this file at the places shown – they remain unchanged.</li>

 <li>Complete the <strong>public static Data[] convert(Object[] objects)</strong> method, which will convert the <strong>Object[]</strong> array <strong>objects </strong>into a <strong>Data[]</strong> array as follows:

  <ol>

   <li>The two arrays should have the same length.</li>

   <li>Any <strong>Single</strong> or <strong>List</strong> objects should be placed unchanged into the new array. (Use only a shallow copy.)</li>

   <li>Any <strong>String</strong> should become a <strong>List</strong> object containing all of the numbers that can be found (as separate tokens) in the <strong>String</strong>. Use a <strong>Scanner</strong> to scan the <strong>String</strong> for numbers. Non-numbers should be ignored. [Note: any number will give true for <strong>hasNextDouble()</strong>.] Assume that the resulting <strong>List</strong> will always have from 0 to <strong>MAX_LIST_SIZE</strong> values in it. Remember that a <strong>List</strong> object must always be a full list, not a partially-full list.</li>

   <li>Any other kind of object should be changed into a <strong>List</strong> object containing a length-0 array.</li>

  </ol></li>

 <li>The new result should be:</li>

</ol>

<strong>      The sum of everything is 45.4       There are 11 values in total. </strong>





