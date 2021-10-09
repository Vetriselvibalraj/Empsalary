import java.util.*;
public class EmpSalary {
public static void main(String[] args)
{
Scanner sc = new Scanner(System.in);
System.out.println("Enter the Employee ID :");

int id=sc.nextInt();
System.out.println("Enter the Employee Name :");
String name= sc.next();
System.out.println("Enter the Employee Department :");
String dept= sc.next();
Employee emp= new Employee(id, name, dept);

System.out.println("Enter the basic pay");
int basic = sc.nextInt();

System.out.println("*********The Employee Details are********");
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
System.out.println("Employee ID: "+EmpId);
System.out.println("Employee Name: "+Name);

System.out.println("Employee Dept:" +Dept);
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
System.out.println("Basic Salary:\t" + basic);
System.out.println("Dearness Allowance:\t"+ da);
System.out.println("House Rent Allowance:\t"+ hra);
System.out.println(&quot;Other Allowances:\t&quot; + oth);
System.out.println("Total Salary is:" + total);
}
}

