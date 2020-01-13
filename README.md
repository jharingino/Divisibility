# Divisibility
display the quotient of divisor up to the max dividend

# developed by: Joshua Hans Aringino
# subject to further optimization
def getquotient():
	quotient = int(max_value / divisible_by)	# calculate quotient
	for i in range(1, quotient+1):
		prod = divisible_by * i
		print(int(prod))
	remainder = round((max_value % divisible_by), 2)	# get remainder
	print("remainder of:", abs(remainder),'\n')

while True:

	divisible_by = float(input("Enter Divisibility: "))	# divisor
	max_value = float(input("Enter Max Value: "))		# dividend

	if max_value >= divisible_by:		# dividend validation
		max_value = max_value
		
	else:
		print("Invalid Max Value!")		# invalid dividend

	while True:
		try:
			if (max_value / divisible_by) >= divisible_by:	# non-zero division validation
				getquotient()
				break
				
			elif divisible_by == max_value > 0:		# validate equal value
				quotient = int(max_value / divisible_by)
				print(quotient)
				break
				
			else:
				getquotient()
				break
				
		except ZeroDivisionError:
			print("ZeroDivisionError occured!")		# address zero division error
			break
			
