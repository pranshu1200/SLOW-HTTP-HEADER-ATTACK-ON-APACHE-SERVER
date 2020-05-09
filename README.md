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
    update repos first:
        sudo apt-get update
    Install the tool:
        sudo apt-get install slowhttptest

# Submissions


