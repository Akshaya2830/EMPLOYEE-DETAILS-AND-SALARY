# EMPLOYEE-DETAILS-AND-SALARY
# Function to input employee details
def get_employee_details():
    name = input("Enter Employee Name: ")
    emp_id = input("Enter Employee ID: ")
    department = input("Enter Department: ")
    basic_salary = float(input("Enter Basic Salary: "))
    return name, emp_id, department, basic_salary

# Function to calculate salary details
def calculate_salary(basic_salary):
    hra = basic_salary * 0.20     # 20% House Rent Allowance
    da = basic_salary * 0.10      # 10% Dearness Allowance
    pf = basic_salary * 0.12      # 12% Provident Fund deduction

    gross_salary = basic_salary + hra + da
    net_salary = gross_salary - pf

    return hra, da, pf, gross_salary, net_salary

# Function to print salary slip
def print_salary_slip(name, emp_id, department, basic, hra, da, pf, gross, net):
    print("\n============== EMPLOYEE SALARY SLIP ==============")
    print("Employee Name   :", name)
    print("Employee ID     :", emp_id)
    print("Department      :", department)
    print("-----------------------------------------------")
    print("Basic Salary    : Rs.", basic)
    print("HRA (20%)       : Rs.", hra)
    print("DA (10%)        : Rs.", da)
    print("PF Deduction    : Rs.", pf)
    print("-----------------------------------------------")
    print("Gross Salary    : Rs.", gross)
    print("Net Salary      : Rs.", net)
    print("================================================")
# Main Program
name, emp_id, department, basic = get_employee_details()
hra, da, pf, gross, net = calculate_salary(basic)
print_salary_slip(name, emp_id, department, basic, hra, da, pf, gross, net)
