# Process customer record 
## Prompt
A program is required to read a customer’s name, a purchase amount and a tax code. 
The tax code has been validated and will be one of the following:
    0  tax exempt (0%)
    1  state sales tax only (3%)
    2  federal and state sales tax (5%)
    3  special sales tax (7%)
The program must then compute the sales tax and the total amount due,and print the customer’s name, purchase amount, sales tax and total amount due.

## Pseudocode

<pre>
Module Main
	Declare String name
	Declare Real purchase_amt
	Declare Integer tax_code
	Declare Real sales_tax
	Declare Real total

	Display "Enter the customer's name: "
	Input name
	Display "Enter the purchase amount: "
	Input purchase_amt
	Display "Enter the tax code. Must be an integer between 0 and 3: "
	Input tax_code

	// calculate sales tax depending on given code
	If(tax_code == 0) Then
		Set sales_tax = 0.0
	Else if(tax_code == 1)
		Set sales_tax = 0.03
	Else if(tax_code == 2)
		Set sales_tax = 0.05
	Else if(tax_code == 3)
		Set sales_tax = 0.07

	// calculate total cost
	Set total = purchase_amt * (1 + sales_tax)

	// display output
	Display "The customer's name is ", name
	Display "The purchase amount is ", purchase_amt
	Display "The sales tax is ", sales_tax * 100, " %."
	Display "The total amount due is ", total
End Main
</pre>
