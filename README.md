# cloud_engr-Ass1
Your login name: altschool i.e., home directory /home/altschool. The home directory contains the following sub-directories: code, tests, personal, misc Unless otherwise specified, you are running commands from the home directory.

sudo useradd -m -s /usr/bin/bash altschool
sudo passwd altschool
sudo usermod -aG sudo altschool
sudo su - altschool
mkdir code tests personal misc
cd /home/altschool/tests
cd ..
cd tests
cd ..
echo Hello A > /home/altschool/misc/fileA
cat /home/altschool/misc/fileA
cd misc
touch fileB
cp fileA fileC
mv fileB fileD
tar -cvf misc.tar *
gzip misc.tar
sudo useradd -m -s /usr/bin/bash/leiman
sudo passwd leiman
sudo passwd --expire 0 leiman
sudo useradd -s /usr/bin/sbash/nologin




  
