# Case-Control-Structure
You can use multiple if...elif statements to perform a multiway branch. However, this is not always the best solution, especially when all of the branches depend on the value of a single variable.  Shell supports case...esac statement which handles exactly this situation, and it does so more efficiently than repeated if...elif statements.


#This below line is called shebang
#!/bin/bash 
echo choose any options

echo 1=date
echo 2=Formatting listing with hidden files
echo 3=ip address of a machine
echo 4=Hostname of a machine
echo 5=show current working directory
echo 6=check ports
echo 7=cronological listing of jobs
echo 8=disk free
echo 9=locate standard files
echo 10=check the cpu status
echo 11=check the all listed users
echo 12=check kernal vesrion

read choice

case $choice in

        1)date;;
        2)ls -al;;
        3)ifconfig;;
        4)hostnamectl;;
        5)pwd;;
        6)netstat -ntlp;;
        7)crontab -l;;
        8)df;;
        9)whereis;;
        10)free -h;;
        11)ls /home;;
        12)uname -r;;
        *)echo invalid option

esac

