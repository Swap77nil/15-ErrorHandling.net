# 15-ErrorHandling.net<br>
15 //c# pgm to demonstrate error handling using try , catch and finally block//<br>
using System;<br>
namespace Exercises<br>
{<br>
class ExceptionHandling<br>
{<br>
static void Main(string[] args)<br>
{<br>
Age a = new Age();<br>
try<br>
{<br>
a.displayAge();<br>
}<br>
catch (AgeIsNegativeException e)<br>
{<br>
Console.WriteLine("AgeIsNegativeException: {0}", e.Message);<br>
}<br>
finally<br>
{<br>
Console.WriteLine("Execution of Finally block is done.");<br>
}<br>
}<br>
}<br>
}<br>
public class AgeIsNegativeException : Exception<br>
{<br>
public AgeIsNegativeException(string message) : base(message)<br>
{<br>
}<br>
}<br>
public class Age<br>
{<br>
int age = -5;<br>
public void displayAge()<br>
{<br>
if (age < 0)<br>
{<br>
throw (new AgeIsNegativeException("Age cannot be negative"));<br>
}<br>
else<br>
{<br>
Console.WriteLine("Age is: {0}", age);<br>
}<br>
}<br>
}<br>

OUTPUT:-<br>
![image](https://user-images.githubusercontent.com/98145032/154630895-75920c41-503a-417c-a6c5-d1496795c030.png)

