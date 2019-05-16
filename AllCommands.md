# Commands With Examples


##	ls’ Command Examples in Linux

-	ls : 
-	ls -l : long listing
-	ls -ls : size option
- 	ls -a : Hidden files
-	ls -F : will add the ‘/’ Character at the end each directory
-	ls -lh : Human readable size format
-	ls -r : reverse
-	ls -R : Recursive
-	ls -ltr : last modification date
-	ls -i : inode number
-	ls -n : UID and GID
-	ls -l /tmp/
-	alias ls="ls -lh"
-	unalias ls


##	 Examples of ‘cd’ Command in Linux

-	cd /usr/local
-	cd - :Switch back to previous directory where you working earlier
-	cd .. 
-	cd -- :	Show last working directory from where we moved
-	cd ~ 
-	cd . or cd ./ : no use of in General
-	cd ../../../../../home/avi/Desktop/  : relative path switching
-	cd /etc/v*	: forgot the name of directory and not supposed to use TAB
-	cd /home/av? :forgot the name of directory and not supposed to use TAB

##	 ‘dir’ Command with Different Options and Arguments in Linux

-	# dir [OPTION] [FILE]
-	# dir /
-	# dir /etc
-	# dir
-	# dir -1 : To list one file per line use -1 option as follows.
-	# dir -a : all files including hidden files
-	# dir -al : hidden files with listing
-	# dir -d /etc : Directory contnets
-	# dir -dl /etc
-	# dir -il : inode number 
-	# dir -shl : size hunam format
-	# dir -ashlS /home/kone : all size human long list Size
-	# dir -ashlt /home/kone
-	# dir -R
	
##	Examples of Linux “Touch” Command

-	touch sheena
-	touch sheena meena leena : multiple files
-	touch sheena meena leena :  Change File Access and Modification Time to current time
-	touch -c leena : avoid creating new files
-	touch -m leena : change only modification time to current time
-	touch -c -t YYDDHHMM leena : Explicitly Set the Access and Modification times
-	touch -c -t 12101730 leena	: Explicitly Set the Access and Modification times
-	touch -r leena meena : using time-stamp of existing file to new file
- 	touch -t YYMMDDHHMM.SS tecmint : Create a File using a specified time
-	touch -t 201212101830.55 tecmint


##	Copy command cp

-	alias cp='cp -gR' : progress bar to be appear all the time while copying add the following lines to your  ~/.bashrc
-	alias mv='mv -g'
-	mv --progress-bar Songs/ /data/



##	12 Useful “df” Commands to Check Disk Space in Linux

-	The “df” command displays the information of 
	-	device name
	-	total blocks
	-	total disk space
	-	used disk space
	-	available disk space and mount points on a file system.
-	df
-	df -a :it also displays information of dummy file systems along with all the file system disk usage and their memory utilization
-	df -h : human readable format
-	df -hT /epwf1 : Type -> nfs, xfs, tmpfs
-	df -h
-	df -m


##	10 Useful du (Disk Usage) Commands to Find Disk Usage of Files and Directories
-	“du” (Disk Usage)  used to check the information of disk usage of files and directories on a machine
-	The du command has many parameter options that can be used to get the results in many formats

-	du  /home/tecmint
-	du -h /home/tecmint : human format
- 	du -sh /home/tecmint : summary with human readable format
-	du -ch /home/tecmint: The “-c” flag provides a grand total usage disk space at the last line



##	35 Practical Examples of Linux Find Command

-	find . -name sample.txt
-	find /home -name sample.txt
-	find /home -iname sample.txt
-	find / -type d -name sample
-	find . -type f -name tecmint.php
-	find . -type f -name "*.php"
-	find . -type f -perm 0777 -print
-	find . -type f ! -perm 0777
-	find / -perm 2644 : Find all the SGID bit files whose permissions set to 644.
-	find / -perm 1551 : Find all the Sticky Bit set files whose permission are 551.
-	find / -perm /u=s
-	find / -perm /u=r
-	find / -perm /g=s :Find all SGID set files.
-	find / -type f -perm 0777 -print -exec chmod 644 {} \;
-	find / -type d -perm 777 -print -exec chmod 755 {} \;
-	find . -type f -name "tecmint.txt" -exec rm -f {} \;
-	find . -type f -name "*.txt" -exec rm -f {} \;
-	find /tmp -type d -empty


##	Examples of Linux grep Command

-	grep –v “#”  /etc/apache2/sites-available/default-ssl
-	find . –name “*.mp3” | grep –i JayZ | grep –vi “remix”
-	ifconfig | grep –A 4 eth0
- 	ifconfig | grep  -B 2 UP
-	ifconfig | grep –C 2 lo
-	grep –n “main” setup..py : Shows line numbers
-	ifconfig | grep –c inet6 : count number of lines matching pattern
-	grep –r “function” *
-	ifconfig | grep –w “RUNNING” : –w option to grep searches for the entire pattern that is in the string
-	ifconfig | grep –w “RUN”
-	zgrep –i error /var/log/syslog.2.gz
-	grep –E
-	fgrep –f file_full_of_patterns.txt file_to_search.txt :
	-	The fgrep searches a file or list of files for a fixed pattern string
	- 	It is the same as grep –F
	-	A common way of using fgrep is to pass a file of patterns to it


##	Head command

-	head [options] [file(s)] : Syntax
-	head /etc/passwd /etc/shadow
-	head /etc/passwd 
-	head -n5 /var/log/yum.log
-	head  -5 /var/log/yum.log

## tail command

-	tail [options] [filenames]
-	tail access.log error.log
-	tail access.log 
-	tail -5 access.log

##	cat command

-	cat [options] [filenames] [-] [filenames]
-	cat /etc/passwd 

	-	echo 'Hi Tecmint-Team' > 1 
	-	echo 'Keep connected' > 2 
	-	echo 'Share your thought' > 3 
	-	echo 'connect us tecmint.com@gmail.com' > 4
	
-	cat 1 2 3 4 > 5
-	cat 5
-	cat > tecmint.txt
-	cat > test.txt << end
-	cat avi.txt > avi1.txt
-	cat month
-	tac month


## 6 WC - Word Count commands

-	wc -l : Prints the number of lines in a file.
-	wc -w : prints the number of words in a file.
-	wc -c : Displays the count of bytes in a file.
-	wc -m : prints the count of characters from a file.
-	wc -L : prints only the length of the longest line in a file.	

-	wc -c tecmint.txt
-	wc -m tecmint.txt
-	wc -L tecmint.txt
-	wc -l tecmint.txt
-	wc -w tecmint.txt

	

##	Pydf 

-	The “pydf” (Python Disk File System) is an advanced command line tool and a good alternative to Linux “df comand”. 
-	It is used to display the amount of used and available disk space on a Linux file systems, same like df command, but in different colours.
- 	The output of the pydf command can be customizable according to your needs
	
	-	sudo apt-get install pydf
	-	pydf
	-	pydf -a
	-	pydf -h
	
	
##	Rename -	A Command Line Tool For Renaming Multiple Files in Linux

-	We often use “mv” command to rename a single file in Linux. 
-	However, renaming multiple or group of files quickly makes it very difficult task in a terminal.
-	Linux comes with a very powerful built-in tool called rename.
- 	The rename command is used to rename multiple or group of files
	-	rename files to lowercase
	-	rename files to uppercase 
	-	overwrite files using perl expressions


##	‘echo’ command in Linux

-	echo [option(s)] [string(s)]
-	echo Tecmint is a community of Linux Nerds
-	$ x=10
-	echo The value of variable x = $x 
-	The ‘-e‘ option in Linux acts as interpretation of escaped characters that are backslashed
-	Using option ‘\b‘ – backspace with backslash interpretor ‘-e‘ which removes all the spaces in between
	-	echo -e "Tecmint \bis \ba \bcommunity \bof \bLinux \bNerds"
		
		-	TecmintisacommunityofLinuxNerds 
-	Using option ‘\n‘ – New line with backspace interpretor ‘-e‘ treats new line from where it is used.
	-	echo -e "Tecmint \nis \na \ncommunity \nof \nLinux \nNerds" 	
		
			Tecmint 
			is 
			a 
			community 
			of 
			Linux 
			Nerds 

		
-	Using option ‘\t‘ – horizontal tab with backspace interpretor ‘-e‘ to have horizontal tab spaces
	-	echo -e "Tecmint \tis \ta \tcommunity \tof \tLinux \tNerds" 
		
			Tecmint 	is 	a 	community 	of 	Linux 	Nerds 
			


##	uname -a

-	The “uname” command stands for (Unix Name), print detailed information about the machine name, Operating System and Kernel.

		Linux tecmint 3.8.0-19-generic #30-Ubuntu SMP Wed May 1 16:36:13 UTC 2013 i686 i686 i686 GNU/Linux

##	sudo

-	The “sudo” (super user do) command allows a permitted user to execute a command as the superuser or another user,
- 	as specified by the security policy in the sudoers list
	
##	chown

-	chown command is used to change the ownership of files 

	-	chown server:server sample.txt
	
##	apt	

-	The Debian based “apt” command stands for (Advanced Package Tool)
- 	Apt is an advanced package manager for Debian based system (Ubuntu, Kubuntu, etc.)
-	that automatically and intelligently search, install
- 	update and resolves dependency of packages on Gnu/Linux system from command line


		apt-get install mplayer
		apt-get update
	

##	tar

-	The “tar” command is a Tape Archive is useful in creation of archive, in a number of file format and their extraction


	-	c –> Creates a new .tar archive file.
	-	v –> Verbosely show the .tar file progress.
	-	f –> File name type of the archive file.
	-	x -> xtract the tar file
	-	r -> append the file 
	-	t -> list the files of tar file
	-	z -> to create compress gzip archive file
	-	j -> to create compressed file in the bz2 format
	
-	Create tar Archive File
	
		tar -cvf tecmint-14-09-12.tar /home/tecmint/
	
-	To create a compressed gzip archive file we use the option as z

		tar cvzf MyImages-14-09-12.tar.gz /home/MyImages
		
-	Create tar.bz2 Archive File
		
	-	The bz2 feature compress and create archive file less than the size of the gzip
	-	To create highly compressed tar file we use option as j
	
		tar cvfj Phpfiles-org.tar.bz2 /home/php
		
-	Untar tar Archive File
	
	-	To untar or extract a tar file, just issue following command using option x (extract)
	
		tar -xvf public_html-14-09-12.tar	
		
-	Uncompress tar.gz Archive File

		tar -xvf thumbnails-14-09-12.tar.gz

-	Uncompress tar.bz2 Archive File

		tar -xvf videos-14-09-12.tar.bz2

-	 List Content of tar Archive File

		tar -tvf uploadprogress.tar
		tar -tvf staging.tecmint.com.tar.gz
		tar -tvf Phpfiles-org.tar.bz2
		

-	Untar Single file from tar File
			
		tar -xvf cleanfiles.sh.tar cleanfiles.sh
		tar -zxvf tecmintbackup.tar.gz tecmintbackup.xml
		tar -jxvf Phpfiles-org.tar.bz2 home/php/index.php

-	Untar Multiple files from tar, tar.gz and tar.bz2 File
			
		tar -xvf tecmint-14-09-12.tar "file 1" "file 2" 
		tar -zxvf MyImages-14-09-12.tar.gz "file 1" "file 2" 
		tar -jxvf Phpfiles-org.tar.bz2 "file 1" "file 2"	
		
-	Extract Group of Files using Wildcard

		tar -xvf Phpfiles-org.tar --wildcards '*.php'
		tar -zxvf Phpfiles-org.tar.gz --wildcards '*.php'	
		tar -jxvf Phpfiles-org.tar.bz2 --wildcards '*.php'
		

-	Add Files or Directories to tar Archive File

	-	To add files or directories to existing tar archived file we use the option r (append)
	
		tar -rvf tecmint-14-09-12.tar xyz.txt


		
##	ftp 

-	ftp domain.com
-	ftp 192.168.0.1
-	ftp user@ftpdomain.com
-	ftp -nv IPADDRESS or hostname

	-	Login with User and Password
		
		user
		password
		
	-	Working with Directories
		
		ls
		cd directory
		
		
-	 Downloading files with FTP
			
		lcd /home/user/yourdirectoryname
		get file
		mget *.xls
		put file
		
		
		
##	How to find IP Address from Hostname

-	ping hostname
-	nslookup hostname
-	grep hostname /etc/hosts
-	ifconfig -a
