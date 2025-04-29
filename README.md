# cpsc457-assignment-3-solved
**TO GET THIS SOLUTION VISIT:** [CPSC457 Assignment 3 Solved](https://www.ankitcodinghub.com/product/cpsc-457-assignment-3-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;116183&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CPSC457  Assignment 3 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
Improve the performance of an existing single-threaded calcpi program by converting it to a multi-threaded implementation. Download the starter code, compile it, and run it:

$ git clone https://gitlab.com/cpsc457/public/pi-calc.git

$ cd pi-calc

$ make

$ ./calcpi

Usage: ./calcpi radius n_threads where 0 &lt;= radius &lt;= 100000 and 1 &lt;= n_threads &lt;= 256

The calcpi program estimates the value of π using an algorithm that is very similar to the one described in https://en.wikipedia.org/wiki/Approximations_of_%CF%80#Summing_a_circle’s_area. The estimation algorithm is implemented inside the function count_pi() in file calcpi.cpp.

The included driver (main.cpp) parses the command line arguments, calls count_pi() and prints the results. It takes 2 command line arguments: an integer radius and number of threads. For example, to estimate the value of π using radius of 10 and 2 threads, you would run it like this:

$ ./calcpi 10 2

Calculating PI with r=10 and n_threads=2

count: 317 PI: 3.17

You need to find a way to parallelize the algorithm without using any synchronization mechanisms, such as mutexes, semaphores, atomic types, etc. You are only allowed to create and join threads.

I suggest you try to parallelize the outer loop. Give each thread roughly equal number of rows in which to count the pixels. Then sum up the counts from each thread. Your overall algorithm could look like this:

• Create separate memory area for each thread (for input and output), e.g. struct Task { int start_row, end_row, partial_count; …}; Task tasks[256];

• Divide the work evenly between threads, e.g. for(int i = 0 ; I &lt; n_threads ; I ++) { tasks[i].start_row = … ; tasks[i].end_row = … ;

}

• Join the threads.

• Combine the results of each thread into final result – i.e. return the sum of all partial_counts.

Assume 0 ≤𝑟𝑟 ≤ 100,000 and 1 ≤𝑛𝑛𝑛𝑛ℎ𝑟𝑟𝑟𝑟𝑟𝑟𝑟𝑟𝑟𝑟 ≤ 256.

Time your multi-threaded solution from Q1 with 𝑟𝑟 = 50000 using the time command on linuxlab.cpsc.ucalgary.ca. Record the real-time for 1, 2, 3, 4, 6, 8, 12, 16, 24 and 32 threads. Also record the timings of the original single-threaded program.

A. Make a table with these timings, and a bar graph, both formatted similar to these:

The numbers in the above table and graph are random. Your timings should look different.

B. When you run your implementation with N threads, you should see N-times speed up compared to the original single threaded program. Do you observe this in your timings for all values of N?

C. Why do you stop seeing the speed up after some value of N?

Convert a single-threaded program detectPrimes to a multi-threaded implementation. Start by downloading the single-threaded code, then compile it and run it:

$ git clone https://gitlab.com/cpsc457/public/detectPrimes.git

$ cd detectPrimes/

$ make

$ cat example.txt

0 3 19 25

4012009 165 1033

$ ./detectPrimes 5 &lt; example.txt

Using 5 threads.

Identified 3 primes:

3 19 1033

Finished in 0.0000s

$ seq 100000000000000000 100000000000000300 | ./detectPrimes 2

Using 2 threads.

Identified 9 primes:

100000000000000003 100000000000000013 100000000000000019 100000000000000021

100000000000000049 100000000000000081 100000000000000099 100000000000000141

100000000000000181 Finished in 5.6863s

The detectPrimes program reads integers in range [2, 263− 2] from standard input, and then prints out the ones that are prime numbers. The first invocation example above detects prime numbers 3, 19 and 1033 in a file example.txt. The second invocation uses the program to find all primes in the range [1017, 1017 + 300].

detectPrimes accepts a single command line argument – a number of threads. This parameter is ignored in the current implementation because it is single-threaded. Your job is to improve the execution time of detectPrimes by making it multi-threaded, and your implementation should use the number of threads given on the command line. To do this, you will need to re-implement the function:

std::vector&lt;int64_t&gt; detect_primes(const std::vector&lt;int64_t&gt; &amp; nums, int n_threads);

which is defined in detectPrimes.cpp. The function takes two parameters: the list of numbers to test, and the number of threads to use. The function is called by the driver (main.cpp) after parsing the standard input and command line. Your implementation should use n_threads number of threads. Ideally, if the original single-threaded program takes time 𝑇𝑇 to complete a test, then your multi-threaded implementation should finish that same test in 𝑇𝑇/𝑁𝑁 time when using 𝑁𝑁 threads. For example, if it takes 10 seconds to complete a test for the original singlethreaded program, then it should take your multi-threaded program only 2.5 seconds to complete that same test with 4 threads. To achieve this goal, you will need to design your program so that:

• each thread is doing roughly equal amount of work for all inputs;

• overall your multi-threaded implementation does the same amount of work as the singlethreaded version; and

• the synchronization mechanisms you utilize are efficient.

• output correct results; and

• achieve near optimal speedup for the given number of threads and available cores.

Hint 1 – bad solution (do not implement this)

A bad solution would be to parallelize the outer loop of the algorithm, and assign a fixed portion of the numbers to each thread to check. This is a terrible solution because it would not achieve speedups on many inputs, for example where all hard numbers are at the beginning, and all the easy ones at the end. Your program would then likely give all hard numbers to one thread and would end up running just as slowly as the single-threaded version.

Hint 2 – simple solution

I strongly suggest you start by implementing this simple solution first, and only attempt the more difficult approaches after your simple solution already works.

Hint 3 – very good solution

Hint 4 – best solution

This builds on top of the hint 3 above, but it also adds thread cancellation. You need cancellation for cases where one of the threads discovers the number being tested is not a prime, so that it can cancel the work of the other threads. Thread cancellation sounds simple to implement, but it does take considerable effort to get it working correctly.

Time the original single-threaded detectPrimes.cpp as well as your multi-threaded version on three files: medium.txt, hard.txt and hard2.txt. For each of these files, you will run your solution 6 times, using 1, 2, 3, 4, 8 and 16 threads. You will record your results in 3 tables, one for each file, formatted like this:

m edium.txt

# threads Observed timing Observed speedup compared to original

Expected speedup

original program 1.0 1.0

1 1.0

2 2.0

3 3.0

4 4.0

8 8.0

16 16.0

The ‘Observed timing’ column will contain the raw timing results of your runs. The ‘Observed speedup’ column will be calculated as a ratio of your raw timing with respect to the timing of the original single-threaded program. Once you have created the tables, explain the results you obtained. Are the timings what you expected them to be? If not, explain why they differ.

Submission

Submit the following files to D2L for this assignment.

Do not submit a ZIP file. Submit individual files.

calcpi.cpp solution to Q1

detectPrimes.cpp solution to Q3

report.pdf answers to all written questions

General information about all assignments:

3. After you submit your work to D2L, verify your submission by re-downloading it.

http://www.ucalgary.ca/pubs/calendar/current/k-5.html.

9. Here are some examples of what you are not allowed to do for individual assignments: you are not allowed to copy code or written answers (in part, or in whole) from anyone else; you are not allowed to collaborate with anyone; you are not allowed to share your solutions with anyone else; you are not allowed to sell or purchase a solution. This list is not exclusive.

Appendix 1 – approximate grading scheme for Q3
