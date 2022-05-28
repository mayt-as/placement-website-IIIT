

> Steps to update placement website.
1. Fork/clone this repo
2. Make changes in your local
3. push changes to this repository
4. SSH to server and run script.

## To run localy
    
```bash
     npm install -g http-server
     http-server -p 8080
```

## run script
```bash
1. SSH to server (IP: 14.139.198.171)
2. cd ankit
3. bash push.bash
```
---

# Script Info.
Check it this direcetories exist, If not create this.
1. /home/administrator/tmp_dump/source

```bash
# home/administrator/ankit/push.bash
#!/bin/bash

cd /home/administrator/tmp_dump/source
git clone https://github.com/dj999dash/placement-website-IIIT.git
sudo cp -R  /home/administrator/tmp_dump/source/*/* /var/www/html/
rm -rf /home/administrator/tmp_dump/source/*
```



---

# Script customization.
```bash
#!/bin/bash

# tempoaray source directly to store new code.
cd <--temporary source directory-->

# Clone new code from repository
git clone <-- repository to clone from -->

# copy all data from soruce directy recursively to server directory.
sudo cp -R  <--same temporary source directy-->/*/* /var/www/html/

# remove all content from remporary srouce directy
rm -rf <--same temporary source directy-->/*
```

## Remeber to make the script executable
```bash
chmod +x filename.sh
```
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQCy7qNalXxXcblFEYWHwq7/9Kbff0atqxl/yX1kCp9GIOSqWLBF2of8GwSlqYeCLvQYUxNCVFgl+FIvavSYttkFL8ugEFxqxPKZ1Yj+qGug4SuztHYf3T7u+JUzCZ6eEfFSyCCYAgaib39e7MAedfzjS5yx2Fl3Sp7qDDMBp325n2q5r4jcpBYzp6+gjkK1Rt7Ej4Qw4+e1Qp2sqcTvaA2nLbmLNXBi8ntPdrdpSzCT/JObRTPsT0RzisiWbZ8X6DOcs//bql9bTlmEYxO98kNE2cio+XK0X7lwh5jxu6Ya8rl3v35MoyowAuri8iBrzu+p1KRqvfkFNJuzOUjkDPHtBMGaOS66+CwBU2PK5SACNx2CmlykZPIWwr14AIl6vpbHaN7mGEFWKmgNdzOiJ1sHtn+ZCOLe2rLikojYh7Rubz+6SR1zJsTg7T2pidKTtUDPicixy74lQ2TFVyavScF5nq49faHMw1EcDTne0yRwL1ywo+JJQDs9ZGEzxMC/Hyc= pawan@sam_sepio