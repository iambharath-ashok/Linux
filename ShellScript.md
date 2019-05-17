# Shell Scipting

-	The first line of the shell script file begins with a "sha-bang" (#!) 
-	which is not read as a comment, followed by the full path where the shell interpreter is located
-	#!/bin/bash

##	Variables

		#!/bin/bash
		# Change this code
		BIRTHDATE=
		Presents=10
		BIRTHDAY=
		PRICE_PER_APPLE=5
		MyFirstLetters=ABC
		
##	Passing Arguments to the Script

-	./bin/my_shopping.sh apple 5 banana 8 "Fruit Basket" 15
-	echo $3 --> results with: banana

		BIG=$5

		echo "A $BIG costs just $6" --> results with: A Fruit Basket costs just 15

-	The variable $# holds the number of arguments passed to the script

		echo $# --> results with: 6

-	The variable $@ holds a space delimited string of all arguments passed to the script
-	$* holds all the arguments as the single arguments

##	Arrays

-	An array can hold several values under one name
-	Array naming is the same as variables naming
- 	An array is initialized by assign space-delimited values enclosed in ()


		my_array=(apple banana "Fruit Basket" orange)
		new_array[2]=apricot
		
-	The total number of elements in the array is referenced by ${#arrayname[@]}

		my_array=(apple banana "Fruit Basket" orange)
		echo  ${#my_array[@]}                   # 4	
		
-	The array elements can be accessed with their numeric index
- 	The index of the first element is 0

		my_array=(apple banana "Fruit Basket" orange)
		echo ${my_array[3]}                     # orange - note that curly brackets are needed
		# adding another array element
		my_array[4]="carrot"                    # value assignment without a $ and curly brackets
		echo ${#my_array[@]}                    # 5
		echo ${my_array[${#my_array[@]}-1]}     # carrot


##	Array-Comparison

	# basic construct
	# array=(value1 value2 ... valueN)
	array=(23 45 34 1 2 3)
	#To refer to a particular value (e.g. : to refer 3rd value)
	echo ${array[2]}  34

	#To refer to all the array values
	echo ${array[@]} 23 45 34 1 2 3

	#To evaluate the number of elements in an array
	echo ${#array[@]} 6
	

##	Basic Operators
	
			































		