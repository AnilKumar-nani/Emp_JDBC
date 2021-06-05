# Emp_JDBC
The requirement is to create a table in database and to insert detailes in java by connecting both.

and to conncet both java and database we will help of driver 

    con=DriverManager.getConnection("jdbc:mysql://localhost:3306/iprime_assignment","root","12345"); 
							String get_empid = "select coalesce((select max(empid)+1 from iprime_assignment.emp1),1) as getid";
							st = con.createStatement();
  and to i have to give choices like insert, display , update age, and exit
  
          System.out.println("1.Insert\n2.Display\n3.Update Age data\n4.Exit");
  
  if the user select the insert option it will ask the detailes of the employee to insert like empid , name, age and designation
  
      System.out.println("Enter Employee Name :");
					String name =sc.next();
					System.out.println("Enter Employee Age :");
					int age = sc.nextInt();
					System.out.println("Enter Employee Desig :");
					String desig = sc.next();
					System.out.println("Enter Employee Sal :");
					int sal = sc.nextInt();
   and to  give the random detailes her i used prepared statement 
   
    ps = con.prepareStatement("insert into emp1 values(?,?,?,?,?)" );
    
and to update the age 

    System.out.println("Enter Employee Name :");
					String name =sc.next();
					System.out.println("Enter Employee Age :");
					int age = sc.nextInt();
					System.out.println("Enter Employee Desig :");
					String desig = sc.next();
				
					con=DriverManager.getConnection("jdbc:mysql://localhost:3306/iprime_assignment","root","12345");  
					ps = con.prepareStatement("update emp1 set age = ? where desig = ? and empname = ? ");
  
