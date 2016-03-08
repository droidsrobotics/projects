<h1>PIX3L PLOTT3R Web Interface</h1>

The ev3 printer now has a web interface where you can type text and draw!

This has been tested using Firefox on Ubuntu.



*   Prerequisites (Ubuntu):
*   
        sudo apt-get update
        sudo apt-get upgrade
        sudo apt-get install apache2 sshpass php5 libapache2-mod-php5 php5-mcrypt

*   The ev3dev version should be the latest. To upgrade:

        sudo apt-get dist-upgrade


*   Download this folder (Ubuntu):
*   
        git clone https://github.com/droidsrobotics/ev3dev.git
        cd ev3dev/PIX3L\ PLOTT3R/server
        cp home_ubuntu/* ~/
        sudo cp -r www_ubuntu/* /var/www/html/

*   Download this folder (EV3):<br>
        <code>git clone https://github.com/droidsrobotics/ev3dev.git</code><br>
        <code>cd ev3dev/PIX3L\ PLOTT3R/server</code><br>
        <code>cp ev3_home/* ~/</code><br>

You will need to replace <code>192.168.43.22</code> in sendprint.py with the ev3's ip address
You will also need to replace <code>robot</code> and <code>maker</code> in sendprint.py and printer.sh with your ev3 username and password.
(printsend.py is on the Ubuntu computer and printer.sh is on the ev3)

*   Run Code (Ubuntu):
  
        cd ~/
        mkdir files
        mkdir lock
        python printer.py &
        python sendprint.py 
        Go to http://localhost/ in Firefox

To manage more than one printer, duplicate printsend.py and run all the versions at once.

