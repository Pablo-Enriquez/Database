# Database
# Pablo Enriquez
# .NET Programming

While the code is still under works and is not fully running at the moment I have an idea of how the code should work and I need to finish it up by next week.

How the code works: 

Namespace and Classes: The code is organized within the DatabaseEnriquez namespace. It defines two classes:

Car: Represents a car model with properties such as Id, Make, Model, and Year.
CarDbContext: Represents the database context class responsible for interacting with the underlying database. It inherits from DbContext.
DbContext Configuration: Within the CarDbContext class, there's a method OnConfiguring that configures the database connection. However, there's an error in the code: CarDbContext should inherit from DbContext, not itself. This should be corrected to avoid compilation errors.

Main Program: The Main method is the entry point of the program. It displays a menu for various operations like adding a car, listing cars, updating a car, removing a car, removing all cars, or exiting the program. The user's choice determines the action to be performed.

AddCar: Adds a new car to the database after taking input for make, model, and year from the user.
ListCars: Lists all cars stored in the database.
UpdateCar: Updates an existing car's details based on the user input for make, model, and year.
RemoveCar: Removes a car from the database based on the user-provided car ID.
RemoveAllCars: Removes all cars from the database.

Limitations (Things to work on for next week):

Error in DbContext Inheritance: As mentioned earlier, there's an error in the code where CarDbContext is incorrectly inheriting from itself. This should be corrected to inherit from DbContext.

User Input Handling: User input is assumed to be valid throughout the code. If the user enters invalid input (e.g., non-numeric values for years), the program will throw exceptions. Proper error handling should be implemented to handle such scenarios gracefully.

Database Connection Configuration: The database connection string is hardcoded within the OnConfiguring method. In a real-world scenario, it's better to externalize such configurations using configuration files or environment variables for better flexibility and security.
