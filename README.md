Installing ROS (desktop-full) Step by Step
After setting up Ubuntu 20.04 ver on your Virtualbox, follow these steps to install ROS successfully:
Open the terminal and write the following command:

" echo "deb http://packages.ros.org/ros/ubuntu focal main" | sudo tee /etc/apt/sources.list.d/ros-focal.list " to add the official ROS Noetic repo to sources.list.


After running the command above, you will see the output: " deb http://packages.ros.org/ros/ubuntu focal main "
######


Next, we will need to add the ROS Noetic keyring to get authenticated ROS packages to install on your Ubuntu, There are two ways to add the official key, and you can choose any of them.

The first is to use apt-key to add the key to be downloaded from the Ubuntu key server. by writing the command below:
"sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654"
if this does not work, you can also try to replace "hkp://keyserver.ubuntu.com:80" with "hkp://pgp.mit.edu:80".
######

The second way is to use curl to download the official ROS key and add it locally. To do this paste the command below:
" curl -sSL 'http://keyserver.ubuntu.com/pks/lookup op=get&search=0xC1CF6E31E6BADE8868B172B4F42ED6FBAB17C654' | sudo apt-key add -", if you see output “OK”, the key is successfully added.
#####


Next, we will need to get the ROS Noetic package information from the repository we just added using apt update, by writing this command:
" sudo apt update "
You will see output like the following, especially the text in bold:
######
Now we are ready to install Noetic on Ubuntu 20.04, To install ros-noetic-desktop-full, run the following: 
" sudo apt install ros-noetic-desktop-full "
After you run the command above, you will see the following output.
######
Press Y and enter or simply press enter to continue installing.
After installing ROS Noetic on your Ubuntu 20.04 computer, we will now set up your environment. To do that, run the command below:
" source /opt/ros/noetic/setup.bash "
To avoid run the command above every time, it is recommended to put it in the .bashrc file located in the home directory ~. To do it run the following:
" echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc "
Last thing you need to do is to verify noetic installation, to do this you need to simply run roscd or roscore. 
#######


Reference:
http://wiki.ros.org/noetic/Installation/Ubuntu
http://wiki.ros.org/Distributions#Noetic_Ninjemys
https://varhowto.com/install-ros-noetic-ubuntu-20-04/
