# epizza
epizza
ePizza company wants to build a point of sale system for their retail customers through which they can accept pizza orders. Your assignment is to build the system that satisfies the following requirements.
The system should allow the users to customize the pizza based on the following options
•	Choose the pizza size. This can be either Small, Medium or Large
•	Choose the pizza base. This can be either Normal, Pan Crust, Thin Crust or Cheesy Bites
•	Choose sauce. This can be either Margarita or Mexican Salsa
•	Choose one or more toppings. The available options are Capsicum, Onion, Tomato, Pineapple, Olive and Jalapeno.
•	Choose cheese: The available options are Mozzarella or Cream Cheese
The price for a small Normal crust is £5.00, Pan crust is £6.00, Thin crust is £6.00 and Cheesy Bites is £7.00. The cost increases by 25% and 50% for medium and large sized pizzas respectively.
No extra charge for sauce.
First two toppings are free of cost. After that each of the topping costs £1.00 for a small pizza, £1.50 for a medium pizza and £2.00 for a large pizza.
The customer can ask for a double cheese. If double cheese is requested, there will be an extra charge of £0.50, £1.00 and £1.50 for small, medium and large size pizzas respectively.
The customer can also provide their email address while placing the order. If no previous orders have been placed for the supplied email address, the system should apply a new customer discount of 10% on the total order cost. 
For the new customer discount requirement, it is necessary for the system to persist the email address. In real application, it would be a database but for the first version (i.e. this assignment), it is sufficient to use a simple file system based persistence.  Feel free to use any format (plain text, XML, JSON etc.) of your choice.
A 20% VAT should be applied to the total order cost.
The system should determine the total bill cost based on the above calculations. In real application, the system will return the receipt data to be displayed on a web interface. However, for this exercise, it is sufficient to print the receipt in the console or to write it into a file.
Kindly note that it is not required to implement a user interface. Simple console based application taking a file as an input is sufficient.
Submission guidelines
1.	The solution should be in Java programming language.
2.	Must be a working solution with following sample orders passing.
3.	Though the working solution is MUST and important, evaluation criteria will also depend on
a.	Use of object oriented principles
b.	 Follow clean code principles like DRY, KISS, YAGNI etc.
c.	Use of right design patterns, where applicable.
d.	Automated unit test cases.
e.	Naming conventions.
4.	Try to use standard Java libraries as much as possible except where third party libraries are unavoidable. JUnit can be used for unit test cases however.
5.	The source code for the solution should be uploaded to GitHub (https://github.com/). Create an account GitHub if you don’t have one already. 
6.	If you are making any assumptions regarding the requirement, please document the same and upload it along with the solution.
7.	Please specify the dependencies (third party libraries, version etc.), if any. 

Examples:

Example 1: Input file
SMALL|NORMAL|MARGARITA|CAPSICUM,ONION,OLIVE|MOZZARELLA
LARGE|PAN|MARGARITA|ONION,PINEAPPLE|CREAM,DOUBLE
EMAIL:email@example.com

Example 1: Expected output
SMALL|NORMAL|MARGARITA|CAPSICUM,ONION,OLIVE|MOZZARELLA	£6.00
LARGE|PAN|MARGARITA|ONION,PINEAPPLE|CREAM,DOUBLE	£10.50
New customer discount (10%)	-£1.65
Order total	£14.85
VAT (20%)	£2.97
Total	£17.82

EXPLANATION
For first pizza:
Small pizza with normal crust costs £5.00
First two toppings are free.
Third topping for small pizza costs £1.00
So, the total for line item 1 is £6.00
For second pizza:
	Large pizza with Pan crust costs £9.00
Only two toppings are ordered, so no extra cost for toppings.
	Double cheese for large pizza costs £1.50
	So, the total for line item 2 is £10.50
Total is £16.50 (i.e. £6.00 + £10.50)

Since an email address is provided and no previous orders have been placed with this email address, apply a 10% discount on the total cost.

Add a 20% VAT to the order total.

Example 2: Input file
SMALL|NORMAL|MARGARITA|CAPSICUM,ONION,OLIVE|MOZZARELLA
LARGE|PAN|MARGARITA|ONION,PINEAPPLE|CREAM,DOUBLE

Example 2: Expected output
SMALL|NORMAL|MARGARITA|CAPSICUM,ONION,OLIVE|MOZZARELLA	£6.00
LARGE|PAN|MARGARITA|ONION,PINEAPPLE|CREAM,DOUBLE	£10.50
Order total	£16.50
VAT (20%)	£3.30
Total	£19.80

EXPLANATION
The calculations are same Example 1. However “New Customer Discount” is not applicable in this case as there was no email address provided in the input.

Example 3: Input file
SMALL|NORMAL|MARGARITA|CAPSICUM,ONION,OLIVE|MOZZARELLA
LARGE|PAN|MARGARITA|ONION,PINEAPPLE|CREAM,DOUBLE
EMAIL:email@example.com

Example 3: Expected output
SMALL|NORMAL|MARGARITA|CAPSICUM,ONION,OLIVE|MOZZARELLA	£6.00
LARGE|PAN|MARGARITA|ONION,PINEAPPLE|CREAM,DOUBLE	£10.50
Order total	£16.50
VAT (20%)	£3.30
Total	£19.80

EXPLANATION
The calculations are same Example 1. However “New Customer Discount” is not applicable in this case as the email address has been used already for another order
