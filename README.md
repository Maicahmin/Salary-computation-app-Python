# Salary-computation-app-Python


Create 3 Modules for this app

The first module is GrossSalary.py will handle the function for computing the gross
salary.

The second module is SalaryDeductions.py will handle the function for computing the deductions

The last module NetSalary.py will be responsible for computing the net salary.

The user will input the following (Name, Hour, Loan, Health Insurance).

Tax(12% of the gross salary) and Rate(500/hr) is fixed

--------------------------------------------------------------------------------------------------------

from GrossSalary import rate

from SalaryDeductions import tax, TotalDeductions

from NetSalary import net


name = str(input("Enter Name: "))

hour = int(input("Hour: "))

gross = rate(hour)


print()

print("Gross Salary:", gross)


print()

print("Tax:", tax(gross))

loan = float(input("Loan: "))

insurance = float(input("Insurance: "))

deductions = TotalDeductions(tax(gross), insurance, loan)

print()


print("Total Deduction: ", deductions)

print()

print("Net Salary: ", net(gross, deductions))

--------------------------------------------------------------------------
#Module 1 GrossSalary.py

def rate(hour):

    return 500 * hour
    
--------------------------------------------------------------------------
#Module 2 SalaryDeduction.py

def tax(gross):

    return gross * 0.12

def TotalDeductions(tax2, insurance, loan):

    return tax2 + insurance + loan
    
--------------------------------------------------------------------------
#Module 3 NetSalary.py

def net(gross, deductions):

    return gross - deductions
    
