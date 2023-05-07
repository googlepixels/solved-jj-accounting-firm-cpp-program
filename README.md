Download Link: https://assignmentchef.com/product/solved-jj-accounting-firm-cpp-program
<br>
During the tax season, every Friday, the J&amp;J accounting firm provides assistance to people who prepare their own tax returns. Their charges are as follows:

If a person has low income (&lt;= 25,000) and the consulting time is less than or equal to 30 minutes, there are no charges; otherwise, the service charges are 40% of the regular hourly rate for the time over 30 minutes.

For others, if the consulting time is less than or equal to 20 minutes, there are no service charges; otherwise, service charges are 70% of the regular hourly rate for the time over 20 minutes.

(For example, suppose that a person has low income and spent 1 hour and 15 minutes, and the hourly rate is $70.00. Then the billing amount is 70.00 * 0.40 * (45 / 60) = $21.00.)

Write a program in C++ that prompts the user to enter the hourly rate, the total consulting time, and whether the person has low income. The program should output the billing amount. Your program must contain a function that takes as input the hourly rate, the total consulting time, and a value indicating whether the person has low income. The function should return the billing amount. Your program may prompt the user to enter the consulting time in minutes. Below is the code i have at the moment. I keep getting a “timed out” message on the testcase i am trying to pass it through. The subject is over User Defined Functions..

#include&lt;iostream&gt;

#include &lt;iomanip&gt;

using namespace std;

double calculateBill(int income, int consultingMinutes, double hourlyRate);

int main()

{

int income, consultingMinutes;

double hourlyRate;

cout &lt;&lt; “Please enter the clients income: $” ;

cin &gt;&gt; income; cout &lt;&lt; “Please enter the consulting time in minutes: “;

cin &gt;&gt; consultingMinutes;

cout &lt;&lt; “Please enter the hourly rate: $”;

cin &gt;&gt; hourlyRate; cout &lt;&lt; fixed &lt;&lt; showpoint &lt;&lt; setprecision(2);

cout &lt;&lt; “Your total bill ammount comes to: $” &lt;&lt; calculateBill(income, consultingMinutes, hourlyRate) &lt;&lt; endl;

return 0;

}

double calculateBill(int income, int consultingMinutes, double hourlyRate)

{

if (income &lt;= 25000) { if (consultingMinutes &lt;= 30) return 0; else return hourlyRate * 0.40 * ((consultingMinutes – 30) / 60);

}

else { if (consultingMinutes &lt;= 20) return 0;

else return hourlyRate * 0.70 * ((consultingMinutes – 20) / 60);

}

}