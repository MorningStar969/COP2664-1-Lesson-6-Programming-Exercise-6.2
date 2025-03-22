# COP2664-1-Lesson-6-Programming-Exercise-6.2
This is a GitHub repository link for the second Programming Assignment from Module 6

// This program is created to calculate the bonus of an employee based on the number of years they have worked at the company.

import Foundation

func calculateBonus(name: String?, salary: Double, yearsOfService: Int) { // Defines a function called calculateBonus that takes in a name, salary, and years of service as parameters.
    guard let name = name, !name.isEmpty, salary > 0, yearsOfService >= 0 else { // Checks if the name, salary, and years of service are valid.
        print("Error: Invalid input. Salary and years of service must be valid.")
        return
    }
    // If the input is valid, the function calculates the bonus based on the number of years of service and prints the result.
    var bonusPercentage: Double = 0.0
    if yearsOfService >= 5 { 
        bonusPercentage = 0.2
    } else if yearsOfService >= 3 {
        bonusPercentage = 0.1
    } else if yearsOfService >= 1 {
        bonusPercentage = 0.05
    }
    // If the employee has worked for 5 or more years, they receive a 20% bonus. If they have worked for 3 or more years, they receive a 10% bonus. If they have worked for 1 or more years, they receive a 5% bonus.
    let bonusAmount = salary * bonusPercentage
    print("Employee: \(name)")
    print("Salary: $\(salary)")
    print("Years of Service: \(yearsOfService)")
    print("Bonus: $\(bonusAmount)")
}
calculateBonus(name: "Oswald", salary: 2000.0, yearsOfService: 4)
calculateBonus(name: "Daisy", salary: 4000.0, yearsOfService: 8)
calculateBonus(name: "Henry", salary: 3000.0, yearsOfService: -2)
calculateBonus(name: "George", salary: -10000.0, yearsOfService: 11)
calculateBonus(name: "Wendy", salary: 7000.0, yearsOfService: 0)
