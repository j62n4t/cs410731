java c
AP/ITEC 2610 Fall 2024 Section E
Assignment 01
Task 1: Implement ContractEmployee Class
The company employs contract-based workers who are paid based on the number of hours they work. Every contract employee has a fixed number of hours they can work upon registration. When the initial number of hours runs out, they can work additional hours, but they are paid extra for overtime.
Please write a Java program (ContractEmployee.java) to manage contract employees. The ContractEmployee class should have the following public interface:
1.  public ContractEmployee(String name, int hours): A constructor to set up the employee’s name and the initial number of working hours allowed. The parameter   hours must be positive; if not, initialize the number of hours to 0.
2.  public String getName(): An accessor to return the employee’s name.
3.  public int getRemainingHours(): An accessor to return the number of remaining hours.
4.  public boolean isValid(): A method to check if the employee is still valid (i.e., true if the number of remaining hours is greater than 0; false otherwise).
5.  public boolean addHours(int additionalHours): A method to add
additionalHours to the remaining hours. Returns true if the top-up succeeds and   false otherwise. The top-up succeeds only if the additionalHours is non-negative.
6.  public boolean logWorkHour(): A method that deducts 1 from the number of
remaining hours when the employee is valid. Returns true if the charge succeeds and false otherwise. The charge succeeds only if the employee has remaining hours.
7.  public boolean overtimeAllowed(): A method that indicates whether overtime
work is allowed. Returns true if the employee has logged all initial hours; otherwise, returns false.
Write a tester program Task1EmployeeTester to test the class you have written. Follow the examples given in class (e.g., BankAccountTester) and create an object from the ContractEmployee class. Test the public interface of your class thoroughly (each public method must be tested at least once). For accessor methods, print out the expected return value and the return value of your method to compare. This tester class is not to be submitted for marking, but it is beneficial to ensure your ContractEmployee class works as intended.
Task 2: Introduce Employee Class
The company now introduces a new type of employee called FullTimeEmployee. Full-time employees are salaried workers who have access to all office facilities, but they have a fixed working schedule. In addition, they can attend internal training programs and are entitled to company benefits. Unlike contract employees, full-time employees do not have a limited number of working hours.
Since the company now employs different types of workers (and more types might be added in the future), you should implement a hierarchy of classes to represent different types of employees. At the top of the hierarchy, you must define an abstract class called Employee, defining methods common to all types of employees. The class Employee should have the following public interface:
1.  public Employee(String name, String type): A constructor to set up the employee’s name and type.
2.  public String getName(): An accessor to return the employee’s name.
3.  public String getType(): An accessor to return a string representing the type of employee.
4.  public abstract boolean isValid(): An abstract method to be overridden by subclasses to determine if the employee is valid.
5.  public boolean officeAccess(): Set an initial return value and override it in the subclasses.
6.  public boolean trainingAllowed(): Set an initial return value and override it in the subclasses.<代 写AP/ITEC 2610 Fall 2024 Section E Assignment 01Java
代做程序编程语言br>Task 3: Extend the ContractEmployee to PartTimeEmployee
Now that you have implemented the ContractEmployee, extend it into a new class PartTimeEmployee. A PartTimeEmployee is an employee who works fewer hours and may only have access to certain benefits.
The PartTimeEmployee class should:
•    Inherit from the abstract class Employee.
•    Retain the core functionality of tracking hours from ContractEmployee.
•    Implement its own behavior. based on the abstract methods defined in Employee.
The PartTimeEmployee class should have the following public interface:
1. public PartTimeEmployee(String name, int hours): A constructor to set up the employee’s name and hours, inheriting from Employee and using the hours functionality from ContractEmployee.
2. public boolean isValid(): Return true if the employee has remaining hours, false otherwise.
3. public boolean officeAccess(): Return true because part-time employees have office access.
4. public boolean trainingAllowed(): Return false because part-time employees cannot attend internal training programs.
Task 4: Implement FullTimeEmployee Class
The FullTimeEmployee class represents salaried workers with unlimited working hours and access to various benefits. The class should extend Employee and have its own specific behavior, while maintaining the common structure of all employees.
The FullTimeEmployee class should have the following public interface:
1.  public FullTimeEmployee(String name): A constructor to set up the employee’s name and type (initialize the type as Full-Time).
2.  public boolean isValid(): Always return true because full-time employees do not have a limited working period.
3.  public boolean officeAccess(): Return true because full-time employees have access to all office facilities.
4.  public boolean trainingAllowed(): Return true because full-time employees can attend internal training programs.
5.  public boolean benefitsAllowed(): Return true because full-time employees are entitled to company benefits.
Write a tester program Task2EmployeeTester to test the classes PartTimeEmployee and FullTimeEmployee. Ensure that all public methods are tested.
Submission Instructions:
Submit the following source files (compress into one .zip file):
• ContractEmployee.java
• Employee.java
• PartTimeEmployee.java
• FullTimeEmployee.java
Ensure that:
• You submit only .java files, not .class files.
•   Your code compiles under the command line (without an IDE), and you do not include package statements.
• Name the classes and the methods the same as provided in the question exactly.
Marking Scheme:
Style. (Variable naming, indentation  layout): ____ / 10
JavaDoc Comments                                      ____ / 10
Code Compiles?                                           ____(yes/no)
Successful Execution of Test Cases                 ____ / 80
Total                                                           ____ / 100
•   Your assignment will be given a zero mark if only the compiled files (.class files) are submitted. Please make sure to submit the source files (.java files).
•   Please make sure your code compiles under the command line (i.e., without an
IDE). Do not put any package statement at the beginning of your source file. If you are using an IDE, this is especially important because some IDEs put your code under a particular package for your project. Any code that does not compile under the command line can only receive at most 20/100. Remarking requests like “ ...but the code works on  my computer/in my IDE” will not be entertained.







         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
