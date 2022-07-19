
<h1>Installing ROS (desktop-full) Step by Step</h1>
<p>After setting up Ubuntu 20.04 ver on your Virtualbox, follow these steps to install ROS successfully:</p>



<h2>Step 1 - Set up ROS Noetic repo for Ubuntu 20.04</h2>
<p>To install Noetic on Ubuntu 20.04, first we will need to add the official ROS Noetic repo to <code>sources.list</code> by running the following command:</p>
      
      <code> echo "deb http://packages.ros.org/ros/ubuntu focal main" | sudo tee /etc/apt/sources.list.d/ros-focal.list </code>

  

<h2>Step 2 — Add official ROS keyring</h2>
<p>Next, we will need to add the ROS Noetic keyring to get authenticated ROS packages to install on your Ubuntu, There are two ways to ad the official key, and you can choose any of them.</p>

<p>The first is to use apt-key to add the key to be downloaded from the Ubuntu key server. by writing the command below:</p>

      <code>sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654</code>
   
The second way is to use <code>curl</code> to download the official ROS key and add it locally. To do this paste the command below:
      
      <code>curl -sSL 'http://keyserver.ubuntu.com/pks/lookup?op=get&search=0xC1CF6E31E6BADE8868B172B4F42ED6FBAB17C654' | sudo apt-key add</code>



<h2> Step 3 — Update ROS package index </h2>
<p>Next, we will need to get the ROS Noetic package information from the repository we just added using apt update, by writing this command</p>
  
    <code>sudo apt update</code>  
  

<h2>Step 4 — Install ROS Noetic Desktop Full</h2>
<p>Now we are ready to install Noetic on Ubuntu 20.04, To install ros-noetic-desktop-full, run the following:</p>
    
    <code>sudo apt install ros-noetic-desktop-full</code>



<h2> Step 5 - Set up ROS Noetic environment </h2>
<p>After installing ROS Noetic on your Ubuntu 20.04 computer, we will now set up your environment. To do that, run the command below:</p>
    
    <code>source /opt/ros/noetic/setup.bash</code>

<p>To avoid run the command above every time, it is recommended to put it in the .bashrc file located in the home directory ~. To do it run
the following:</p>
    
    <code>echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc</code>

      
  
<h2> Step 6 - Verify Noetic installation </h2>
<p>We can simply run <code>roscd</code>. You can see the current directory of your prompt is changed to where we installed Noetic
<code>/opt/ros/noetic</code>.</p>
