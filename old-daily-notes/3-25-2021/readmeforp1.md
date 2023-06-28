# Weston Davidson P1 - SineShop

## Project Overview
SineShop is a store application developed in mind for a chain of stores that sell analogue and digital synthesizers. This project involved designing with ASP.NET MVC architecture, and implemented a number of technologies for security, design, and scalability purposes.

## Implemented Features
- Customer addition - managerial
- Customer search - managerial
- Product ordering
    - Customers can purchase multiple different products
- Order history - managerial
- Inventory updates/replenishing - managerial
- Persistent customer carts per location
    - Customers can change their location and have their cart dynamically update for new order processing

## Technologies Used
- Serilog - Logging
- Moq -  Unit Testing
- ASP.NET Identity – login/authentication
- ASP.NET MVC – Architecture
- Azure Cloud Services – App hosting
- Azure Devops – Pipeline
- SonarCloud – Code Quality Assurance
- Google Cloud Platform – APIs & Services
- PostgreSQL – Relational Database

## Getting Started
1. Use the command `git clone https://github.com/210215-USF-NET/Weston_Davidson-P1.git` in your desired directory to clone the necessary files to your system.
1. Run `dotnet run` within a terminal/command prompt within the root directory of the project
    - this will both build and run the program
1. If the application does not open in a web browser on it's own, please navigate to the specified localhost port in your web browser to view the user interface.

## Usage
- Once the program is running, feel free to explore the UI as desired. As a customer, you will need to create an account first to access the system. Once your account has been created and you have logged in, the expected functionalities of most web-based shopping sites should be available to you.

## License
This project is licensed under the MIT License.


- make sure a p3 proposal exists


(load)="GetUser(user.email)

  GetUserByEmail(email:string) : Observable<any>
  {
    return this.http.get<User>(`${this.url}/${email}`, this.httpOptions)
  }



  
  GetUser(userName: string)
  {
    this.userService.GetUserByEmail(userName).subscribe
    (
      foundUser =>
      {
        this.userBackend = foundUser;
      }
    )
  }
