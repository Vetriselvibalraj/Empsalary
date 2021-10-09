import java.util.*;
public class EmpSalary {
public static void main(String[] args)
{
Scanner sc = new Scanner(System.in);
System.out.println(&quot;Enter the Employee ID :&quot;);

int id=sc.nextInt();
System.out.println(&quot;Enter the Employee Name :&quot;);
String name= sc.next();
System.out.println(&quot;Enter the Employee Department :&quot;);
String dept= sc.next();
Employee emp= new Employee(id, name, dept);

System.out.println(&quot;Enter the basic pay&quot;);
int basic = sc.nextInt();

System.out.println(&quot;*********The Employee Details are********&quot;);
emp.printEmployee();
Salary sal = new Salary();
sal.calculateTotal(basic);

}
}
class Employee
{
private int EmpId;
private String Name;
private String Dept;
Employee(int EmpId,String Name,String Dept)
{
this.EmpId=EmpId;
this.Name= Name;
this.Dept=Dept;
}
void printEmployee()
{
System.out.println(&quot;Employee ID: &quot;+EmpId);
System.out.println(&quot;Employee Name: &quot;+Name);

System.out.println(&quot;Employee Dept: &quot; +Dept);
}
}
class Salary
{
private double da;
private double hra;
private double oth;

void calculateTotal(int basic)
{
da = 0.90 * basic;
hra = 0.20 * basic;
oth = 0.10 * basic;
double total = basic + da + hra + oth;
System.out.println(&quot;Basic Salary:\t&quot; + basic);
System.out.println(&quot;Dearness Allowance:\t&quot; + da);
System.out.println(&quot;House Rent Allowance:\t&quot; + hra);
System.out.println(&quot;Other Allowances:\t&quot; + oth);
System.out.println(&quot;Total Salary is: &quot; + total);
}
}

