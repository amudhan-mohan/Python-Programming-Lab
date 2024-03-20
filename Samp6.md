import csv
from collections import defaultdict
def read_csv_file(file_path):
 employees = []
 with open(file_path, 'r') as file:
 reader = csv.DictReader(file)
 for row in reader:
 employees.append(row)
 return employees
def find_highest_paid_employee(employees):
 highest_paid_employee = max(employees, key=lambda x: float(x['salary']))
 return highest_paid_employee
def sort_employees_by_department(employees):
 sorted_employees = sorted(employees, key=lambda x: x['department'])
 return sorted_employees
def calculate_average_salary_by_department(employees):
 department_salaries = defaultdict(list)
 for employee in employees:
 
department_salaries[employee['department']].append(float(employee['salary']))
 average_salaries = {department: sum(salaries) / len(salaries) for 
department, salaries in department_salaries.items()}
 return average_salaries
def main():
 file_path = 'employee_data.csv'
 employees = read_csv_file(file_path)
 highest_paid_employee = find_highest_paid_employee(employees)
 print(f"Highest Paid Employee: {highest_paid_employee['name']} (ID: 
{highest_paid_employee['employee_id']}, Salary: 
{highest_paid_employee['salary']})")
 sorted_employees = sort_employees_by_department(employees)
 print("\nEmployees Sorted by Department:")
 for employee in sorted_employees:
 print(f"{employee['name']} (ID: {employee['employee_id']},
 Department: {employee['department']}, Salary: {employee['salary']})")

 average_salaries = calculate_average_salary_by_department(employees)

 print("\nAverage Salary by Department:")

 for department, avg_salary in average_salaries.items():

 print(f"{department}: {avg_salary:.2f}")

if __name__ == "__main__":

 main()








 Source Code (CSV File):
Note: Save a CSV File as employee_data.csv
employee_id,name,department,salary
1,Sriram ,HR,50000
2,Vasanth,IT,60000
3,Praneeth,HR,55000
4,Suresh,IT,65000
5,Ramesh,Finance,70000
Note: Create and save CSV file and change the directory name to the CSV file directory which 
you created in the python source code and execute.
