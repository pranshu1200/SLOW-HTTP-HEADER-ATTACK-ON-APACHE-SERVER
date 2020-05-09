# SLOW-HTTP-HEADER-ATTACK-ON-APACHE-SERVER
Computer and Network Security course project. A bot to launch typical DOS attack based on HTTP and thread based server vulnerabilities

# Slow HTTP Header vulnerability:
Post incomplete HTTP headers regularly after a certain interval of time.The bot creates large number of HTTP connections to the given web server. Since, a thread based web server has a upper limit on the maximum amount of threads it can handle, eventually we will succeed to create a DOS attack and put down the web server or drastically increase the time to access the web page.

# Tools Required
    Python3
    An Apache web server to attack(Thread based server)
    Wireshark
    SlowHttpTest Tool


# Installing Dependencies:
    pip3 install -r requirements.txt

# Installing WireShark on Ubuntu:
    sudo apt-get install wireshark
    sudo groupadd wireshark
    sudo usermod -a -G wireshark YOUR_USER_NAME
    sudo chgrp wireshark /usr/bin/dumpcap
    sudo chmod 750 /usr/bin/dumpcap
    sudo setcap cap_net_raw,cap_net_admin=eip /usr/bin/dumpcap
    sudo getcap /usr/bin/dumpcap

# Installing SlowHttpTest Tool
    sudo apt-get update
    sudo apt-get install slowhttptest

# Submissions
    main.py : The main function to set up attack parameters for the bot
    target.py : Create a target vector
    connection.py : Set up the connection to the server under attack and get results
    wireshark capture.pcapng : The WireShark capture for the attack on a sample web server.
    COMPUTER AND NETWORK SECURITY – CST 308 REPORT.pdf : Presentation Report on the Attack Bot
    supplementary document prepared by me.pdf : Supplementary text doc
    
 # Usage
    python3 main.py
    enter the ip address of server to be attacked 
    enter the port number
    enter time to wait before posting next incomplete header is made in seconds(the time between sending consecutive set of         incomplete HTTP headers by connections)
    enter the number of concurrent connections to make to the server
    
    The system shows if the given (ip,port) pair is valid or  not , and if its valid then checks if the server vulnerable to the attack(is it thread based Apache server) and the initial lateny.
    Press enter to start the attack 
    
 # Log Info
    Initial Latency to access web page
    Displays when the connections are opened
    The time of sending new set of incomplete headers 
    The when does a timeout occurs.
    
    

