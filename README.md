# Java8

Example on Streams( filter(intermediary operation),mapToDobule(intermediary  operation) and Sum () 

IS sum() stateful or stateless terminal operation ?
    private static Employee[] arrayOfEmps = {
            new Employee(1, "Jeff Bezos", 100000.0),
            new Employee(2, "Bill Gates", 200000.0),
            new Employee(3, "Mark Zuckerberg", 300000.0),
                    new Employee(4, "Jeff Bezos", 100000.0),
                    new Employee(5, "Bill Gates", 200000.0)
    };
    List<Employee> employees = Arrays.asList(arrayOfEmps);
    
    Double sum = employees.stream()
                .filter(w -> w.getName().equalsIgnoreCase("Bill Gates"))
                .mapToDouble(w -> w.getSalary())
                .sum();
        System.out.println("Sum of salary of employees with name : Bill Gates is: " + sum);
