Download Link: https://assignmentchef.com/product/solved-comp2710-project-1
<br>
5/5 - (1 vote)

Goals:

<ul>

 <li>To learn how to implement the concept of “Flow of Control” in C++</li>

 <li>To write a very simple C++ programDescription:You have just purchased a stereo system that cost $1000 on the following credit plan: no down payment, an interest rate of 18% per year (and hence 1.5% per month), and monthly payments of $50. The monthly payment of $50 is used to pay the interest, and whatever is left is used to pay part of the remaining debt. Hence, the first month you pay 1.5% of $1000 in interest. That is $15 in interest. The remaining $35 is deducted from your debt, which leaves you with a debt of $965.00. The next month you pay interest of 1.5% of $965.00, which is $14.48. Hence, you can deduct $35.52 (which is $50–$14.48) from the amount you owe.Write a program that will tell you how many months it will take you to pay off this loan in particular and any loan in general. Your program also needs to calculate the total amount of interest paid over the life of any loan. Use a loop to calculate the amount of interest and the size of the debt after each month. Your program must output the monthly amount of interest paid and remaining debt. Use a variable to count the number of loop iterations and hence the number of months until the debt is zero. You may want to use other variables as well. The last payment may be less than $50 if the debt is small, but do not forget the interest. If you owe $50, then your monthly payment of $50 will not pay off your debt, although it will come close. One month’s interest on $50 is only 75 cents.Here is a sample dialog (where the user input is depicted as Bold, but you do not need to display user input in bold.):</li>

</ul>

Loan Amount: 1000Interest Rate (% per year): 18 Monthly Payments: 50

1

********************************************************** Amortization Table

********************************************************** Month Balance Payment Rate Interest Principal

0 $1000.00 N/A N/A N/A

$50.00 1.50 $15.00 $50.00 1.50 $14.47 $50.00 1.50 $13.94 $50.00 1.50 $13.40 $50.00 1.50 $12.85 $50.00 1.50 $12.30 $50.00 1.50 $11.73 $50.00 1.50 $11.16 $50.00 1.50 $10.57 $50.00 1.50 $9.98 $50.00 1.50 $9.38 $50.00 1.50 $8.77 $50.00 1.50 $8.15 $50.00 1.50 $7.53 $50.00 1.50 $6.89 $50.00 1.50 $6.24 $50.00 1.50 $5.59 $50.00 1.50 $4.92 $50.00 1.50 $4.24 $50.00 1.50 $3.56 $50.00 1.50 $2.86 $50.00 1.50 $2.15 $50.00 1.50 $1.44 $47.83 1.50 $0.71

<pre>N/A$35.00$35.53$36.06$36.60$37.15$37.70$38.27$38.84$39.43$40.02$40.62$41.23$41.85$42.47$43.11$43.76$44.41$45.08$45.76$46.44$47.14$47.85$48.56$47.12</pre>

<ol>

 <li>1  $965.00</li>

 <li>2  $929.47</li>

 <li>3  $893.42</li>

 <li>4  $856.82</li>

 <li>5  $819.67</li>

 <li>6  $781.97</li>

 <li>7  $743.70</li>

 <li>8  $704.85</li>

 <li>9  $665.42</li>

 <li>10  $625.40</li>

 <li>11  $584.79</li>

 <li>12  $543.56</li>

 <li>13  $501.71</li>

 <li>14  $459.24</li>

 <li>15  $416.13</li>

 <li>16  $372.37</li>

 <li>17  $327.95</li>

 <li>18  $282.87</li>

 <li>19  $237.11</li>

 <li>20  $190.67</li>

 <li>21  $143.53</li>

 <li>22  $95.68</li>

 <li>23  $47.12</li>

 <li>24  $0.00</li>

</ol>

**********************************************************

It takes 24 months to pay off the loan. Total interest paid is: $197.83

Your program’s output should match the style of the sample output (including a left lined-up style).

In what follows, you find a second case used to test the correctness of your program.

Loan Amount: 2000Interest Rate (% per year): 12 Monthly Payments: 80

2

******************************************************** Amortization Table

********************************************************

Month Balance

<ol start="0">

 <li>0  $2,000.00</li>

 <li>1  $1,940.00</li>

 <li>2  $1,879.40</li>

 <li>3  $1,818.19</li>

 <li>4  $1,756.38</li>

 <li>5  $1,693.94</li>

 <li>6  $1,630.88</li>

 <li>7  $1,567.19</li>

 <li>8  $1,502.86</li>

 <li>9  $1,437.89</li>

 <li>10  $1,372.27</li>

 <li>11  $1,305.99</li>

 <li>12  $1,239.05</li>

 <li>13  $1,171.44</li>

 <li>14  $1,103.15</li>

 <li>15  $1,034.19</li>

 <li>16  $964.53</li>

 <li>17  $894.17</li>

 <li>18  $823.11</li>

 <li>19  $751.35</li>

 <li>20  $678.86</li>

 <li>21  $605.65</li>

 <li>22  $531.70</li>

 <li>23  $457.02</li>

 <li>24  $381.59</li>

 <li>25  $305.41</li>

 <li>26  $228.46</li>

 <li>27  $150.75</li>

 <li>28  $72.25</li>

 <li>29  $0.00</li>

</ol>

********************************************************

It takes 29 months to pay off the loan. Total interest paid is: $312.98

Payment Rate N/A N/A $80.00 1.00 $80.00 1.00 $80.00 1.00 $80.00 1.00 $80.00 1.00 $80.00 1.00 $80.00 1.00 $80.00 1.00 $80.00 1.00 $80.00 1.00 $80.00 1.00 $80.00 1.00 $80.00 1.00 $80.00 1.00 $80.00 1.00 $80.00 1.00 $80.00 1.00 $80.00 1.00 $80.00 1.00 $80.00 1.00 $80.00 1.00 $80.00 1.00 $80.00 1.00 $80.00 1.00 $80.00 1.00 $80.00 1.00 $80.00 1.00 $80.00 1.00 $72.98 1.00

Interest Principal N/A N/A $20.00 $60.00 $19.40 $60.60 $18.79 $61.21 $18.18 $61.82 $17.56 $62.44 $16.94 $63.06 $16.31 $63.69 $15.67 $64.33 $15.03 $64.97 $14.38 $65.62 $13.72 $66.28 $13.06 $66.94 $12.39 $67.61 $11.71 $68.29 $11.03 $68.97 $10.34 $69.66 $9.65 $70.35 $8.94 $71.06 $8.23 $71.77 $7.51 $72.49 $6.79 $73.21 $6.06 $73.94 $5.32 $74.68 $4.57 $75.43 $3.82 $76.18 $3.05 $76.95 $2.28 $77.72 $1.51 $78.49 $0.72 $72.25

Special Cases:

<ol>

 <li>Please think about how to deal with the last payment, which is smaller than regular payment. For example, in the above table, the regular payments are $80.00 whereas the last payment is only 72.98.</li>

 <li>Your program needs to ensure that regular payments are larger than any monthly interest. For example, in the above amortization table, your program must test if the regular monthly payment (i.e., $80.00) is larger than the monthly interest (e.g., $20.00 in the first month).</li>

 <li>If you do not address the above issue, your program may not terminate in some special cases. See the example below:</li>

</ol>

3

Loan Amount: 2000Interest Rate (% per year): 49.2 Monthly Payments: 80

******************************************************** Amortization Table

********************************************************

Month Balance

<ol start="0">

 <li>0  $2,000.00</li>

 <li>1  $2,002.00</li>

 <li>2  $2,004.08</li>

 <li>3  $2,006.25</li>

 <li>4  $2,008.51</li>

 <li>5  $2,010.85</li>

 <li>6  $2,013.30</li>

 <li>7  $2,015.84</li>

 <li>8  $2,018.49</li>

 <li>9  $2,021.25</li>

 <li>10  $2,024.12</li>

 <li>11  $2,027.11</li>

 <li>12  $2,030.22</li>

 <li>13  $2,033.46</li>

 <li>14  $2,036.84</li>

 <li>15  $2,040.35</li>

 <li>16  $2,044.00</li>

 <li>17  $2,047.80</li>

 <li>18  $2,051.76</li>

 <li>19  $2,055.89</li>

</ol>

… …

Payment Rate N/A N/A $80.00 4.10 $80.00 4.10 $80.00 4.10 $80.00 4.10 $80.00 4.10 $80.00 4.10 $80.00 4.10 $80.00 4.10 $80.00 4.10 $80.00 4.10 $80.00 4.10 $80.00 4.10 $80.00 4.10 $80.00 4.10 $80.00 4.10 $80.00 4.10 $80.00 4.10 $80.00 4.10 $80.00 4.10 …

Interest Principal N/A N/A $82.00 -$2.00 $82.08 -$2.08 $82.17 -$2.17 $82.26 -$2.26 $82.35 -$2.35 $82.45 -$2.45 $82.55 -$2.55 $82.65 -$2.65 $82.76 -$2.76 $82.87 -$2.87 $82.99 -$2.99 $83.11 -$3.11 $83.24 -$3.24 $83.37 -$3.37 $83.51 -$3.51 $83.65 -$3.65 $83.80 -$3.80 $83.96 -$3.96 $84.12 -$4.12 … …

Programming Environment:

Write a short program in C++. Compile and run it using AU server (no matter what kind of text editor you use, please make sure your code could run on AU server, the only test bed we accept is AU server).

Requirements:

<ol>

 <li> Use comments to provide a heading at the top of your code containing your name, Auburn UserID, filename, and how to compile your code. Also describe any help or sources that you used (as per the syllabus).</li>

 <li> Your source code file should be named as “project1_AU UserID.cpp”. Note: You will not lose any point if Canvas automatically changes your file name (e.g. project1-2.cpp) due to your resubmissions.</li>

 <li> No compilation error and no warning messages. 4</li>

</ol>

4.  Usability of your program (e.g., input and output). 5. (40 points) Quality of your source code.