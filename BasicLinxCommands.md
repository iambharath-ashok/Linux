#	Basic Linux/Unix Commands with Examples

-	Listing files (ls)
-	'ls -R


## File Information

	drwxr-x---  2 618796   618796        80 Sep 11  2015 epwf-jboss
	-rw-rw-r--  1 epwf1  qdefault      2117 Nov 11  2013 FileArchiving.sh
	drwxrwxrwx  4 epwf1  invoc96       2048 Mar  9  2011 ftpScripts
	-rw-rw-r--  1 epwf1  qdefault      1531 Nov 13  2013 HCDEFileArchiving1.sh
	-rw-rw-r--  1 epwf1  qdefault      1531 Nov 11  2013 HCDEFileArchiving.sh


-	1st Column	->	File type and access permissions
-	2nd Column	->	# of HardLinks to the File
-	3rd Column	->	Owner and the creator of the file
-	4th Column	->	Group of the owner
-	5th Column	->	File size in Bytes
-	6th Column	->	Date and Time
-	7th Column	->	Directory or File name
	
	
##	Listing Hidden Files
	
-	ls -a
-	cat file1 file2 > newfilename


##	The 'Man' command

-	Man stands for manual which is a reference book of a Linux operating system. 
-	It is similar to HELP file found in popular software


##	'pr' command

-	This command helps in formatting the file for printing on the terminal
-	There are many options available with this command which help in making desired format changes on file

-	Dividing data into columns

	pr -x Filename
	
	-	The '-x' option with the 'pr' command divides the data into x columns.

-	Assigning a header
	
	pr -h "Header" Filename
	
	
-	Denoting all lines with numbers
		
	pr -n Filename
	
		pr -3 bharath
		pr -h "bharath" bharath
		pr -h "bharath" -9 bharath
		pr -h "bharath" -9 -d bharath
		pr -h "bharath" -3 -d bharath
		pr -h "bharath" -3  bharath
		pr -h "bharath" -3 -n bharath
		
	
	
	
-	Printing a file
		
		lp Filename
		lpr Filename
		lp -n10 filename
		lpr 20 filename
		lp -dHPofficejet testfile
		lpr	-phpofficejet testfile
		
		
-	mail

	-	mail -s 'subject' -c 'cc-address' -b 'bcc-address' 'to-address'

-	apt-get

	-	In Linux packages are installed in the form of packages
	-	Installation of packages requires sudo permissions
	-	Command used to install and update packages
	
	
		
