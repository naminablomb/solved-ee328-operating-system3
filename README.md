Download Link: https://assignmentchef.com/product/solved-ee328-operating-system3
<br>



<h1>Salary System</h1>




<h2>1 PROBLEM DESCRIPTION</h2>

<strong>This homework revisits the idea of superclass/subclass, polymorphism. And study how to use</strong>Arrays.sort(). <strong>RememberyouneedtoimplementComparableorComparatortosortyour object array.</strong>

Write a superclass Worker and subclasses HourlyWorker and SalariedWorker. Every worker has a name, a salary rate, and the total salary he got so far from the beginning of his employment. Write a method computePay(int hours) that computes the weekly pay for every worker. An hourly worker get paid the the hourly wage for the actual number of hours worked, of hours is at most 40. If the hourly worker worked more than 40 hours, the excess is paid at double rate. The salaried worker gets paid the hourly wage for 40 hours, no matter what the actual number of hours is. The total salary is just the accumulated value of all the paid salary for the worker. Beside the computePay() method, you can add more methods if you like or think necessary. After creating an array of Worker, I want to sort the array and print out the sorted result. By default, the workers are sorted by their name. You should also be able to sort it by their salary rate, or by the total salary they’ve got. This means if I use Arrays.sort(arrayname) directly, I’m sorting by name. Otherwise I sort by using different comparators.

When print out the information about the workers using System.out.println(worker), I wish to be able to see the worker’s type too, i.e., whether he is HourlyWorker or SalariedWorker, and with his name, salary rate, and total salary.

<h2>2 ALGORITHM</h2>

<h3>2.1 WORKER</h3>

Similar to Project 2, there are three different classes about Workers in this program, Worker, HourlyWorker and SalariedWorker. Obviously HourlyWorker and SalariedWorker are extended from Worker.

<ul>

 <li>Worker</li>

</ul>

This class helps to define basic variables like workerName, workTime, salaryRate and totalSalary. In the meantime methods such as printPay() and computePay() is basically implemented. When executing the constructor to input the information of the worker such as name and salary rate, several checks will be made to make sure that all the inputs are legal.

<ul>

 <li>HourlyWorker</li>

</ul>

It is extended from Worker. Due to the work time threshold the computePay() method is overrided.

<ul>

 <li>SalaryWorker</li>

</ul>

It is also extended from Worker. Because the effective work time is fixed for SalaryWorker the computePay() method is overrided as well.

<h3>2.2 SORT METHODS</h3>

We use <em>Array.sort() </em>to sort by different properties. As is shown in problem description, the workers are sorted by their name by default. In the code we use <em>Array.sort(Workers) </em>directly to sort by name. It is implemented by implementing class Worker from class <em>Comparable</em>. In the <em>compareTo </em>method the string of name is compared by the order of the character. If we get a positive result we define that this one is larger than the compared one.

As for sorting by salary rate and total salary, we use class <em>Comparator </em>rather than <em>Comparable </em>to implement it. In the extended classes <em>salaryRateCompare </em>and <em>totalSalaryCompare </em>method <em>compare </em>is instantiated to create a new rule to compare. To sort by salary rate and total salary using code like <em>Array.sort(Workers, new salaryRateCompare()) </em>is OK.

<h3>2.3 MAIN METHOD</h3>

We create 6 workers initially and define their characteristics by constructor directly. Then we use <em>Array.sort() </em>respectively to sort by different comparators and the display the result.

<h2>3 RESULTS</h2>

<h3>3.1 ENVIRONMENT</h3>

<ul>

 <li>Windows 10</li>

 <li>Java Development Kit 1.8.0_131</li>

 <li>Eclipse</li>

</ul>

3.2 SCREENSHOTS OF THE RESULT

We use command line to compile and execute the program. The result is shown in Fig. 3.1-3.3.

<h3>3.3 THOUGHTS</h3>

This project helps us to learn the difference between <em>Comparable </em>and <em>Comparator</em>. In the meantime we try to implement them by ourselves, which contributes to our coding skills.

Figure 3.1: Screenshot of Salary System (1)

Figure 3.2: Screenshot of Salary System (2)

Figure 3.3: Screenshot of Salary System (3)