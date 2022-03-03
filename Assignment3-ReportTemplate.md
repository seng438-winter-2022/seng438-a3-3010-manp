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

## Range Class

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

## Data Utilities Class

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

In this lab, our goal was to increase the code coverage for the Range class and for the Data Utilities class by creating the new unit tests. So, to increase the code coverage, we used white box testing technique. Initially, when we started the code coverage test on Range Class and Data Utilities class using the test cases that were created using the black box testing, we found that the statement coverage of the Range class was at about 20% , Branch coverage was at 16% and the Condition Coverage was at 25%. Similarly, for the Data Utilities class, the statement coverage was at 52%, Branch Coverage was at 42% and Condition Coverage was 60%.


To increase the Statement coverage of both the Range Class and the Data Utilities class, we created the test cases that can cover all the statements of the Methods of the Range class and the Data Utilities Class. After implementing the new test cases, the statement coverage for the Range Class and for the Data Utilities class was increased to 93% and 100% respectively.  To increase the Branch coverage, we wrote the new test cases as such it covers the most the branches in the Range class and Data Utilities class. We also made DU pairs in some of the methods of the Range and Data Utilities class in order to increase the Branch coverage. After creating and implementing the new test cases, the Branch coverage was increased to 82% for the Range class and was increased to 91.7% for the Data Utilities class.  To increase the Condition Coverage for both the Range and Data Utilities Class, We used MC/DC(Modified Condition-Decision Criterion). This criteria helped in increasing the Condition Coverage of Range class to 100%  and 100% for the Data Utilities class.


# 4 A high level description of five selected test cases you have designed using coverage information, and how they have increased code coverage

The high level descriptions of the five test cases is described as follows:

## Test 1:  testPositiveMarginsForMethodExpandTest in ExpandTest for the Range Class
This test method checks whether the expected output of the expanded range object is equal to actual output when the positive values of lower and upper margin are provided as arguments in the expand method. This test method helps in increasing the statement coverage for the Range class by covering all the lines in the expand method of the Range class.

## Test 2: stmtCoverageTestForMethodHashCode in hashCodeTest for the Range Class

This test method checks if the output1(hashCode) of range object r1 is equal to output2(hashCode) of the range object r1. This test method increases the statement coverage for the Range class by approximately 5%.


## Test 3: testFirstRangeNullForMethodCombine in CombineTest for the Range Class

This test method checks if the range1(null) and range2(not null) is provided as arguments in the combine method and whether the expected output(range2) is equal to actual output obtained from the combine method. This test method increases the branch coverage for the Range Class since it covers one of the branches in the combine method of the range class.

## Test 4: BranchCoverageTestForConstructor in constructorTest for the Range Class

This test method checks whether the constructor throws an illegalArgumentException if the lower limit of the Range Object is greater than the upper limit of the Range Object.
This test method increased the branch coverage for the Range Class by approximately 6% as it covers the missing branch in the Range Class Constructor.

## Test5:testingStringObject() in EqualsTest for the Range Class 

This test Method checks whether a String object is equal to a Range object. This test increases both the branch coverage and the condition coverage. It covers one of the branches in the equals method and also covers decision expression in the equals method and increases the condition coverage by approximately 4% for the Range class.



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

We used the EclEmma coverage tool for finding the coverage for statement, branch, and condition. This tool has many advantages since it can display a green bar which means it has decent coverage or a red bar is displayed and that means more test cases need to be written to get better coverage. Moreover, it also shows the coverage percentage for statement, branch or condition which can be helpful when minimum coverage needs to be reached. The metrics are calculated fast for all related classes (Range and Data Utilities), and the results are directly shown in the Eclipse IDE to view and make changes to the test suite if needed. Another advantage of this tool is that the downloading process is easy as it is a plugin in the Eclipse IDE from the Eclipse Marketplace. It also highlights lines in the code as green (covered lines), red (uncovered lines) and yellow (partially covered). This can also help give a good understanding of which methods require a stronger test coverage.  The tool is easy to use and user-friendly since downloading, using, and understanding the results from this tool can be used to increase the coverage of the test suite. This tool never crashes which makes it a reliable tool to use when finding the coverage for statement, branch, and condition. One of the disadvantages of using EclEmma is that it does not offer support for conditional coverage. Condition coverage is usually used for retrieving the outcome of logical condition and EclEmma not supporting this means that this coverage can not be calculated or be shown. Another disadvantage using a tool such as EclEmma is that it does not guarantee that everything has been tested and moreover the results might not be 100% accurate. 

# 7 A comparison on the advantages and disadvantages of requirements-based test generation and coverage-based test generation.

Requirement-based test generation is a kind of black-box testing, which performs tests based on functional or non-functional requirements without reference to the internal structure of the component or system. On the other hand, coverage-based test generation refers to white-box testing, its procedure to derive or select test cases based on an analysis of the internal structure of a component or system. Both test generations have their own advantages and limitations. When building our testing suites, it is better to use a combination of both testing methods in order to generate better and more comprehensive results.

The general idea of coverage-based test generation is to use technologies such as statement coverage, branch coverage to try to make sure that each line or branch within source code is being executed. It helps to cover any branch or lines to try to find any possible bugs within them which increases the quality of the application. Since some lines with less chance to be executed in common use can be covered. However, the advantage of coverage-based coverage is that it ignores testing the requirements of the system. Since it measures coverage of what has been written, but it cannot identify something that might be missing with the functionality. Also, a 100% line or branch coverage can not ensure bug free code (division by 0 example in lecture). Furthermore, we found that there is sometimes a reachability problem with control flow coverage in our testing. Some lines within the source code are actually not reachable. So that when one does not reach a 100% coverage, sometimes it is difficult to determine the reason.

On the other hand, requirements-based test methods focus on the actual requirement of the system. The advantage is that it directly tests the functionality of the system, any missing or incorrect implementation of functionalities can be easily found. However, one  of the advantages is that it does not actually look at the implementation of the code. Errors existing within some lines which will only be executed at rare conditions can hardly be found.


# 8 A discussion on how the team work/effort was divided and managed

Our group ran the coverage tool in eclipse to get an idea of which methods/functions needed better code coverage. Once this was done, we had split the test cases among ourselves. Girimer worked on CalculateColumnTotalTest, CalculateRowTotalTest, Clone,  CreateNumberArrayTest, CreateNumberArray2DTest, equal, and GetCumluativePercentagestTest. Muhammad worked on getUpperBound, getCentralValue, ExpandTest and Combine. Manpreet worked on Constrain, hashCode, Constructor and Intersects. Tianfan worked on combineIgnoringNaN, isNaNRange, Scale, Shift and expandToInclude. Once we were finished with getting better code coverage for our methods, we verified our findings with our group members.

# 9 Any difficulties encountered, challenges overcome, and lessons learned from performing the lab

By performing this lab, we have learned about white box testing control flow coverage. We had evaluated the functions/methods for org.jfree.data.DataUtilities and org.jfree.data.Range classes so that we can improve our test suite by applying the white box coverage criteria. Our goal was to increase the code coverage for the following: statement coverage, branch coverage and condition coverage. The built-in code coverage tool in eclipse was used for the org.jfree.data.DataUtilities and org.jfree.data.Range and it  was helpful to determine which methods or functions need more stronger coverage. More test cases were created so that we can have better code coverage. We also learned how data-flow coverage is calculated by hand. This was done by calculating the DU-pair coverage for DataUtilities.calculateColumnTotal and Range.combine by following the code in these methods. 

# 10 Comments/feedback on the lab itself

The lab was extremely good in terms of giving a good understanding of white box testing. We learned to improve our test suite so that we can get better code coverage. The benefit of having access to the code gave us the opportunity to cover all the paths so that we can enhance our test suite. The built-in code coverage tool in eclipse gave us a good measurement of statement coverage, branch coverage and condition coverage and based on these findings we were able to design more test cases for our test suite. Also, the lab manual was very detailed and gave us a good overview of what we had to do in the lab and how to do it. The instructions about getting the set-up of the lab were very detailed and easy to follow. 
