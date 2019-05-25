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
	echo ${array[2]}  : output 34

	#To refer to all the array values
	echo ${array[@]} : display all the elements 23 45 34 1 2 3

	#To evaluate the number of elements in an array
	echo ${#array[@]} 6
	

##	Decision Making

- Syntax

	if [ condition ];
	then 
		commands 
	fi
	
	
-	Example 1 : Basic If

		Name = "Bharath"
		if	[ "$Name" = "Bharath" ];
		then
			echo "True My Name is indeed $Name"
		fi
		
-	Example 2 : else

		Name = "Bill"
		if [ "$name" = "John" ];
		then
			echo "My name is indeed John";
		else
			echo "My name is indeed $Name";
		fi
		
-	Example 3 : if else 

		Name = "Bharath";
		if [ "$Name" = "Bill" ];
		then 
			echo "My name is indeed Bill";
		elif ["$Name" = "John" ];
		then
			echo "My name is indeed: $Name";
		else 
			echo "My is name is nothing";
		fi 	
			

##	Types of numeric comparisons

comparison  |  Evaluated to true when
------------|-------------------------
$a -lt $b   | $a < $b
$a -gt $b   | $a > $b
$a -le $b   | $a <= $b
$a -ge $b   | $a >= $b
$a -eq $b   | $a is equal to $b
$a -ne $b   | $a is not equal to $b
			
			
##	Types of string comparisons


comparison | Evaluated to true When
-----------|-----------------------
"$a" = "$b"    | $a is the same as $b
"$a" == "$b"   | $a is the same as $b
"$a" != "$b"   | $a is different from $b
-z "$a"        | $a is empty

##	case structure


-	Syntax

	case "$variable" in
		
		"$condition1")
			commands ...
		;;
		
		"$condition2")
			commands ...
		;;
		
		"$condition3")
			commands ...
		;;
	esac
	

-	simple case bash structure

		mycase=1
		case $mycase in
			1) echo "You selected bash";;
			2) echo "You selected perl";;
			3) echo "You selected phyton";;
			4) echo "You selected c++";;
			5) exit
		esac

##	Loops

-	For Loops

	-	for loops iterate through a set of values until the list is exhausted:

	-	Syntax

		for arg in [list]
		do 
			commands
		done
		
	-	Exmaple 1


		names = (Joe Jony Sara Jenny);
		for N in ${names[@]}; 
		do
			echo "Looping Names: $N"
			
		done
		
	-	Example 2

			#!/bin/sh
			for i in 1 2 3 4 5
			do
			  echo "Looping ... number $i"
			done	
		
			for i in hello 1 * 2 goodbye 
			do
			  echo "Looping ... i is set to $i"
			done
		
	-	Example Set 3

		#!/bin/bash
		echo "Bash version ${BASH_VERSION}..."
		for i in {0..10..2}
		  do 
			 echo "Welcome $i times"
		 done
		 
		 #!/bin/bash
		for i in {1..5}
		do
		   echo "Welcome $i times"
		done
		
		for (( EXP1; EXP2; EXP3 ))
		do
			command1
			command2
			command3
		done
		
		#!/bin/bash
		for (( c=1; c<=5; c++ ))
		do  
		   echo "Welcome $c times"
		done
		
		#!/bin/bash
		for (( ; ; ))
		do
		   echo "infinite loops [ hit CTRL+C to stop]"
		done
		
		for I in 1 2 3 4 5
		do
		  statements1      #Executed for all values of ''I'', up to a disaster-condition if any.
		  statements2
		  if (disaster-condition);
		  then
			break       	   #Abandon the loop.
		  fi
		  statements3          #While good and, no disaster-condition.
		done
		
-	While Loops

	-	Example 1:
	
			#!/bin/sh
			INPUT_STRING=hello
			while [ "$INPUT_STRING" != "bye" ]
			do
			  echo "Please type something in (bye to quit)"
			  read INPUT_STRING
			  echo "You typed: $INPUT_STRING"
			done
			
			#!/bin/sh
			while :
			do
			  echo "Please type something in (^C to quit)"
			  read INPUT_STRING
			  echo "You typed: $INPUT_STRING"
			done
		
		

## Shell Functions


-	Shell functions can be defined with function keyword or just by name
-	Function can be invoked simply by calling function name by passing the params
	
	
	-	Syntax:
	
		function_name () {
			<commands>
		}
		
		
		function function_name {
			<commands>
		}
		
-	Examples:

		#!/bin/bash
		# Basic function
		print_something () {
		echo Hello I am a function
		}
		print_something
		print_something
	

-	Passing Arguments
		
		#!/bin/bash
		# Passing arguments to a function
		print_something () {
		echo Hello $1
		}
		print_something Mars
		print_something Jupiter
		
		
		#!/bin/bash
		# Setting a return status for a function
		print_something () {
		echo Hello $1
		return 5
		}
		print_something Mars
		print_something Jupiter
		echo The previous function has a return value of $?
		
		#!/bin/bash
		# Setting a return value to a function
		lines_in_file () {
		cat $1 | wc -l
		}
		num_lines=$( lines_in_file $1 )
		echo The file $1 has $num_lines lines in it.








		