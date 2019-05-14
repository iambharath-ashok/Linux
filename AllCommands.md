# Commands With Examples


##	ls’ Command Examples in Linux

-	ls : 
-	ls -l : long listing
-	ls -ls : size option
- 	ls -a : Hidden files
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
-	# dir -1
-	# dir -a
-	# dir -al
-	# dir -d /etc
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
-	touch -m leena : change only modification time
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
	-	device name,
	-	total blocks,
	-	total disk space,
	-	used disk space, 
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
-	grep –n “main” setup..py
-	ifconfig | grep –c inet6
-	grep –r “function” *
-	ifconfig | grep –w “RUNNING” : –w option to grep searches for the entire pattern that is in the string
-	ifconfig | grep –w “RUN”
-	zgrep –i error /var/log/syslog.2.gz
-	grep –E
-	fgrep –f file_full_of_patterns.txt file_to_search.txt :
	-	The fgrep searches a file or list of files for a fixed pattern string
	- 	It is the same as grep –F
	-	A common way of using fgrep is to pass a file of patterns to it





	



