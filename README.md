# Library App

## Description

Library App is a simple, modular library management system built with .NET 8.0. It provides a console-based interface for searching patrons, viewing and managing book loans, and handling patron memberships. The application uses JSON files for data storage and is structured for easy extension and testing.

## Project Structure

- AccelerateDevGitHubCopilot.sln
- README.md
- .vscode/
  - launch.json
- src/
  - Library.ApplicationCore/
    - Library.ApplicationCore.csproj
    - Entities/
    - Enums/
    - Interfaces/
    - Services/
  - Library.Console/
    - appSettings.json
    - CommonActions.cs
    - ConsoleApp.cs
    - ConsoleState.cs
    - Library.Console.csproj
    - Program.cs
    - Json/
  - Library.Infrastructure/
    - Library.Infrastructure.csproj
    - Data/
- tests/
  - UnitTests/
    - UnitTests.csproj

## Key Classes and Interfaces

- **ConsoleApp** ([src/Library.Console/ConsoleApp.cs](src/Library.Console/ConsoleApp.cs)):  
  Main entry point for the console UI, manages user interaction and application state.

- **JsonData** ([src/Library.Infrastructure/Data/JsonData.cs](src/Library.Infrastructure/Data/JsonData.cs)):  
  Handles loading, saving, and populating data from JSON files.

- **JsonPatronRepository** ([src/Library.Infrastructure/Data/JsonPatronRepository.cs](src/Library.Infrastructure/Data/JsonPatronRepository.cs)):  
  Implements patron data access using JSON storage.

- **JsonLoanRepository** ([src/Library.Infrastructure/Data/JsonLoanRepository.cs](src/Library.Infrastructure/Data/JsonLoanRepository.cs)):  
  Implements loan data access using JSON storage.

- **IPatronRepository, ILoanRepository** ([src/Library.ApplicationCore/Interfaces/](src/Library.ApplicationCore/Interfaces/)):  
  Interfaces for patron and loan data access, supporting dependency injection and testability.

- **Entities** ([src/Library.ApplicationCore/Entities/](src/Library.ApplicationCore/Entities/)):  
  Core domain models such as Patron, Loan, Book, Author, etc.

## Usage

1. **Build the project:**
   dotnet build AccelerateDevGitHubCopilot.sln

2. Run the console application:
   dotnet run --project src/Library.Console/Library.Console.csproj

3. Follow the on-screen prompts to search for patrons, view details, manage loans, and update memberships.

License
This project is licensed under the MIT License. 