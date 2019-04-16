import matplotlib.pyplot as plt
import math

#Function to give display expenses and compare with income of user
def Budgeting_misc():
    print('Salary Input')
    salary = int(input("SALARY:"))
    Other_income = int(input('OTHER INCOME:'))
    Total_Salary = salary + Other_income
    print("TOTAL INCOME:",Total_Salary)
    print('Expenses Input:')
    print('Housing Expenses:')
    Phone_and_Network = int(input('PHONE AND NETWORK:'))
    Water_Gas_Electricity = int(input('WATER AND GAS SUPPLY:'))
    Rent_House=int(input('HOUSE RENT:'))
    Housing_Expenses= Phone_and_Network+Water_Gas_Electricity+Rent_House
    print('Transportation:')
    Gas_and_Fuel=int(input('GAS AND FUEL:'))
    Car_Insurance=int(input('CAR INSURANCE:'))
    Transportation= Gas_and_Fuel+Car_Insurance
    print('Educational Expenses:')
    College_School_Fees=int(input('COLLEGE FEES:'))
    Educational_Expenses=College_School_Fees
    print('Food ANd Personal:')
    Household=int(input('HOUSEHOLD:'))
    Clothing=int(input('CLOTHING:'))
    Medical=int(input('MEDICAL:'))
    Food_And_Personal=Household+Clothing+Medical
    Other_Expenses=int(input('OTHER EXPENSES:'))
    Total_Expenses=Phone_and_Network+Water_Gas_Electricity+Rent_House+Gas_and_Fuel+Car_Insurance+College_School_Fees+Household+Medical+Clothing+Other_Expenses
    print("TOTAL EXPENSES: ",Total_Expenses)
    #PROGRAM TO PRINT PIE CHART
    Expenses_Lables= [ 'Housing Expenses','Transportation','Educational Expenses','Food And Personal','OTHER EXPENSES']
    Expenses= [ Housing_Expenses, Transportation, Educational_Expenses, Food_And_Personal,Other_Expenses ]
    figureObject , axesObject= plt.subplots()
    axesObject.pie(Expenses,
               labels=Expenses_Lables,
               autopct="%1.2f",
               startangle=90)
    axesObject.axis=('equal')
    plt.show
    if(Total_Expenses>Total_Salary):
        print("SPENDING IS MORE THAN INCOME. \nNO SAVINGS.\nYOU NEED TO REDUCE YOUR SPENDING")
        

    else:
        print("GOOD,YOU ARE SPENDING LESSER THAN YOUR INCOME")
        print("TOTAL SAVINGS:", (Total_Salary-Total_Expenses))
#Budgeting()

Budgeting_misc()

#Function to calculate the present overall investment requirement for a given goal set by the user


def present_value( goal, time, discountrate ):
    current= goal/(1 + discountrate*0.01)**time
    print("The current requirement is: ₹"+str(round(current,2)))

discountrate =float(input("Enter the discount rate (in %): ")) 
years = float(input("Enter period of investment (in years): "))
goal = float(input("Enter Goal: ₹"))

present_value( goal, years, discountrate )

#Function to calculate the time required to achieve goal set by the user given their value of the overall present investment

def time_taken(current,goal,discountrate):
    time=(math.log(goal/current))/(math.log(1 + (discountrate*0.01)))
    print ("Time required to achieve goal is (in years)"+str(round(time,2)))
    
discountrate =float(input("Enter the discount rate (in %): ")) 
current = float(input("Enter your current value of investment: ₹"))
goal = float(input("Enter Goal: ₹"))

time_taken(current,goal,discountrate)

#Function to calculate the monthly investment requirement for a given goal set by the user

discountRate = float(input("Enter Discount rate ( in %): "))
months = float(input("Enter Months: "))
goal = float(input("Enter Goal: ₹"))

def payMeMonthly(x, y,discountRate):
    t = float(y)*(discountRate*0.01)
    u = float(1+discountRate*0.01)
    v = pow(u,x)
    w = float(1/v)
    monthlyPayment = t/(1-w)
    print("Your monthly payment is: ₹"+str(round(monthlyPayment,2)))

payMeMonthly(months,goal,discountRate)

#Function to calculate the time required to achieve goal set by the user given their value of the monthly investment
discountRate =float(input("Enter the discount rate (in %): ")) 
monthlyPayment = float(input("Enter Monthly Payment: ₹"))
goal = float(input("Enter Goal: ₹"))

def monthsRequired(x, y,discountRate):
	q = math.log(1 + discountRate*0.01)
	w = discountRate*0.01*y
	p = math.log(1/(1 - (w/x)))
	months = p/q
	print ("Time required to achieve goal is (in months)"+str(round(months,2)))

#monthlypayment needs to be > goal*discountRate else log(-ve)
if (monthlyPayment>(goal*(discountRate*0.01))):
	monthsRequired(monthlyPayment,goal,discountRate)
else:
	print("Invalid Input")
	print("Input Payment greater than ₹"+str(discountRate*0.01*goal))
    
#Function to calculate the annual investment requirement for a given goal set by the user

def Annual_req(x, y, discountRate):
    annual_pay= float(y)*(discountRate*0.01)/(1-float(1/pow(float(1+discountRate*0.01),x)))
    print("Your annual payment is: ₹"+str(round(annual_pay,2)))
    
years = float(input("Enter period of investment (in years): "))
goal = float(input("Enter your Goal: ₹"))
rate = float(input("Enter Discount Rate ( in %) : "))

Annual_req(years,goal,rate)

#Function to calculate the time required to achieve goal set by the user given their value of the annual investment

def years_req(cash, goal, rate):
    years = math.log(1/(1 - (rate*0.01*goal/cash)))/ math.log(1 + rate*0.01)
    print ("Time required to achieve goal is (in years)"+str(round(years,2)))
    
annual_cash = float(input("Enter the amount you are ready to invest yearly: ₹"))
goal = float(input("Enter your Goal: ₹"))
rate = float(input("Enter the discount rate (in %): "))

#annual payment needs to be > goal*discountRate else log(-ve)
if (annual_cash>(goal*rate*0.01)):
    years_req(annual_cash,goal,rate)
else:
    print("Invalid Input")
    print("Input Payment greater than ₹"+str(rate*goal))
    

#bondFunctions

#function to calculate relative value of bond using yeild to maturity

import math
aRate = float(input("Enter Annual Rate(in %): "))
faceValue = float(input("Enter Face Value: ₹"))
marketValue = float(input("Enter Market Value: ₹"))
maturity = float(input("Enter Maturity in Years: "))

def ytm(w, x, y, z):
	t = (y*x*0.01)
	u = ((y - w)/z)
	v = (y + w)/2
	Yeild = ((t + u)/v)*100
	print("Yeild to Maturity(in %): "+str(round(Yeild,2)))
	if (Yeild>aRate):
		print("This Bond is selling at a discount.")
	elif (Yeild==aRate):
		print("This Bond is selling at par.")
	else :
		print("This Bond is selling at a premium.")
    
ytm(marketValue,aRate,faceValue,maturity)
    
    
 #function to calculate total pnl on bond
 
import math
aRate = float(input("Enter Annual Rate(in %): "))
faceValue = float(input("Enter Face Value: ₹"))
marketValue = float(input("Enter Market Value: ₹"))
maturity = float(input("Enter Maturity in Years: "))
inflation = float(input("Enter Inflation Rate(in %): "))

def don(w, v, x, y, z):
	interest = w*(v*y*0.01) 
	t = (1-(z*0.01))**w
	sellingPrice = x*t
	finalPrice = sellingPrice+interest

	if (finalPrice>marketValue):
		print("This Bond is a good investment.")
		print("Net profit: ₹"+str(round((finalPrice-marketValue),2)))
	else:
		print("This Bond is not a good investment.")
		print("Net loss: ₹"+str(round((finalPrice-marketValue),2)))

don(maturity,faceValue,marketValue,aRate,inflation)
 
 
