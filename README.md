# Employee-Management-System
 Developed an Employee Management System using ASP.NET Core Web API and SQL database. Implemented CRUD operations for employee records, role-based access management, data validation, and RESTful APIs. Used Entity Framework Core for database interaction and GitHub for version control.
## Features
- Employee registration
- Attendance management
- Leave tracking
- Role-based access

## Technologies
- OOP Concepts
- Database Management
- Software Development Principles

## Future Scope
- ASP.NET Core MVC
- SQL Database
- Authentication System
  
CODE(Employee Model)
public class Employee
{
    public int Id { get; set; }
    public string Name { get; set; }
    public string Department { get; set; }
    public decimal Salary { get; set; }
}
CODE(API Controller)
[ApiController]
[Route("api/[controller]")]
public class EmployeeController : ControllerBase
{
    private static List<Employee> employees = new();

    [HttpGet]
    public IActionResult GetAll()
    {
        return Ok(employees);
    }

    [HttpPost]
    public IActionResult Add(Employee employee)
    {
        employees.Add(employee);
        return Ok(employee);
    }
}
