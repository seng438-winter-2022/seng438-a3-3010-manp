**SENG 438 - Software Testing, Reliability, and Quality**

**Lab. Report #3 – Code Coverage, Adequacy Criteria and Test Case Correlation**

| Group \#:23    |     |
| -------------- | --- |
| Manpreet Singh |     |
| Tianfan Zhou   |     |
| Girimer Singh  |     |
| Muhammad Shakeel|     |

(Note that some labs require individual reports while others require one report
for each group. Please see each lab document for details.)

# 1 Introduction

In lab2, we did black box testing with some methods of DataUtilities class and Range class within JFree Chart. We used some testing technologies such as equivalence class testing and boundary testing to test the system. In previous testing, we mainly focused on testing the requirements since we do not know the internal structure of the system. However, only performing black box testing is not good enough. In this lab, we have access to see the actual implementation of the system, which enables us to also perform white box testing to the system to analyze the parts of the code uncovered by our black-box testing. In the first part of this lab, we will try to test the coverage rate (statement, branch, method) of our assignment 2 test suite and record the result as a base line. In part 2, we will perform some manual data flow coverage calculation with method Range.Contain and DataUtilities.calculateColumnTotal to have a better understanding of control flow coverage. In part 3, we will write some more test cases based on white box testing technologies to enhance the coverage rate of our testing. We aim to increase statement, branch and method coverage to be over 90%, 70% and 60% respectively. Both black box testing and white box testing is important because they can be complementary to each other. Combining using both testing methods can result in more reliable and comprehensive test cases.


# 2 Manual data-flow coverage calculations for X and Y methods



<p align="center">
  <img width="400" src="https://github.com/seng438-winter-2022/seng438-a3-3010-manp/blob/main/images/Pic1.png" alt="Material Bread logo">
</p>
<p align="center">
   Figure 1- Method: Range.Combine Diagram

</p>


<p align="center">
  <img width="600" src="https://github.com/seng438-winter-2022/seng438-a3-3010-manp/blob/main/images/Pic2.png" alt="Material Bread logo">
</p>
<p align="center">
   Figure 2- def and use for statements
</p>

<p align="center">
  <img width="600" src="https://github.com/seng438-winter-2022/seng438-a3-3010-manp/blob/main/images/Pic3.png" alt="Material Bread logo">
</p>
<p align="center">
   Figure 3- DU-Pair for each variable 
</p>
 
 
 <p align="center">
  <img width="600" src="https://github.com/seng438-winter-2022/seng438-a3-3010-manp/blob/main/images/Pic4.png" alt="Material Bread logo">
</p>
<p align="center">
   Figure 4- DU Pair Coverage
</p>

<p align="center">
  <img width="600" src="https://github.com/seng438-winter-2022/seng438-a3-3010-manp/blob/main/images/Pic5.png" alt="Material Bread logo">
</p>
<p align="center">
   Figure 5- Method: DataUtilities.calculateColumnTotal Diagram
</p>

<p align="center">
  <img width="600" src="https://github.com/seng438-winter-2022/seng438-a3-3010-manp/blob/main/images/Pic6.png" alt="Material Bread logo">
</p>
<p align="center">
   Figure 6- def and use for statements
</p>

<p align="center">
  <img width="600" src="https://github.com/seng438-winter-2022/seng438-a3-3010-manp/blob/main/images/Pic7.png" alt="Material Bread logo">
</p>
<p align="center">
   Figure 7- DU-Pair for each variable 
</p>

<p align="center">
  <img width="600" src="https://github.com/seng438-winter-2022/seng438-a3-3010-manp/blob/main/images/Pic8.png" alt="Material Bread logo">
</p>
<p align="center">
   Figure 8- DU Pair Coverage
</p>


# 3 A detailed description of the testing strategy for the new unit test


Text…

# 4 A high level description of five selected test cases you have designed using coverage information, and how they have increased code coverage

Text…


# 5 A detailed report of the coverage achieved of each class and method (a screen shot from the code cover results in green and red color would suffice)

<p align="center">
  <img width="600" src="https://github.com/seng438-winter-2022/seng438-a3-3010-manp/blob/main/images/Pic9.png" alt="Material Bread logo">
</p>
<p align="center">
   Figure 9- Branch Coverage for Range Class
</p>


<p align="center">
  <img width="600" src="https://github.com/seng438-winter-2022/seng438-a3-3010-manp/blob/main/images/Pic10.png" alt="Material Bread logo">
</p>
<p align="center">
   Figure 10- Condition Coverage for Range Class
</p>

<p align="center">
  <img width="600" src="https://github.com/seng438-winter-2022/seng438-a3-3010-manp/blob/main/images/Pic11.png" alt="Material Bread logo">
</p>
<p align="center">
   Figure 11- Statement Coverage for Range Class
</p>

<p align="center">
  <img width="600" src="https://github.com/seng438-winter-2022/seng438-a3-3010-manp/blob/main/images/Pic12.png" alt="Material Bread logo">
</p>
<p align="center">
   Figure 12- Coverage Table for Range Class
</p>

<p align="center">
  <img width="600" src="https://github.com/seng438-winter-2022/seng438-a3-3010-manp/blob/main/images/Pic13.png" alt="Material Bread logo">
</p>
<p align="center">
   Figure 13- Branch Coverage for DataUtilities  
</p>


<p align="center">
  <img width="600" src="https://github.com/seng438-winter-2022/seng438-a3-3010-manp/blob/main/images/Pic14.png" alt="Material Bread logo">
</p>
<p align="center">
   Figure 14- Statement Coverage for DataUtilities  
</p>

<p align="center">
  <img width="600" src="https://github.com/seng438-winter-2022/seng438-a3-3010-manp/blob/main/images/Pic15.png" alt="Material Bread logo">
</p>
<p align="center">
   Figure 15- Condition Coverage for DataUtilities  
</p>
Text…

# 6 Pros and Cons of coverage tools used and Metrics you report

Text…

# 7 A comparison on the advantages and disadvantages of requirements-based test generation and coverage-based test generation.

Text…

# 8 A discussion on how the team work/effort was divided and managed

Text…

# 9 Any difficulties encountered, challenges overcome, and lessons learned from performing the lab

Text…

# 10 Comments/feedback on the lab itself

Text…
