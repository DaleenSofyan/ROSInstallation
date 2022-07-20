
<h1>Installing ROS (desktop-full) Step by Step</h1>
<p>After setting up Ubuntu 20.04 ver on your Virtualbox, follow these steps to install ROS successfully:</p>




<h2>Step 1 - Set up ROS Noetic repo for Ubuntu 20.04</h2>
<p>To install Noetic on Ubuntu 20.04, first we will need to add the official ROS Noetic repo to <code>sources.list</code> by running the following command:</p>
      
    echo "deb http://packages.ros.org/ros/ubuntu focal main" | sudo tee /etc/apt/sources.list.d/ros-focal.list
    
<p>After running the command above, you will see the output: <code>deb http://packages.ros.org/ros/ubuntu focal main</code>.</p>




<h2>Step 2 — Add official ROS keyring</h2>
<p>Next, we will need to add the ROS Noetic keyring to get authenticated ROS packages to install on your Ubuntu, There are two ways to ad the official key, and you can choose any of them.</p>

<p>The first is to use apt-key to add the key to be downloaded from the Ubuntu key server. by writing the command below:</p>

    sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654

If you see the following output starting with executing, it means the key is successfully added:

<pre class="wp-block-preformatted" style="position: relative;">Executing: /tmp/apt-key-gpghome.mdMVphTCAR/gpg.1.sh --keyserver hkp://keyserver.ubuntu.com:80 --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
gpg: key F42ED6FBAB17C654: public key "Open Robotics <a href="mailto:info@osrfoundation.org">info@osrfoundation.org</a>" imported
gpg: Total number processed: 1
gpg: imported: 1<div class="open_grepper_editor" title="Edit &amp; Save To Grepper"></div></pre>

The second way is to use <code>curl</code> to download the official ROS key and add it locally. To do this paste the command below:
      
    curl -sSL 'http://keyserver.ubuntu.com/pks/lookup?op=get&search=0xC1CF6E31E6BADE8868B172B4F42ED6FBAB17C654' | sudo apt-key add
    
<p>If you see output <code>OK</code>, the key is successfully added.</p>




<h2> Step 3 — Update ROS package index </h2>
<p>Next, we will need to get the ROS Noetic package information from the repository we just added using apt update, by writing this command</p>
  
    sudo apt update  
    
You will see output like the following, especially the text in bold:

<pre class="wp-block-preformatted" style="position: relative;">Hit:1 http://security.ubuntu.com/ubuntu focal-security InRelease
Hit:2 http://dl.google.com/linux/chrome/deb stable InRelease
<strong>Hit:3 http://packages.ros.org/ros/ubuntu focal InRelease
</strong>Hit:4 http://archive.ubuntu.com/ubuntu focal InRelease
Hit:5 https://download.docker.com/linux/ubuntu bionic InRelease
Hit:6 http://archive.ubuntu.com/ubuntu focal-updates InRelease
Hit:7 http://archive.ubuntu.com/ubuntu focal-backports InRelease
Reading package lists… Done
Building dependency tree
Reading state information… Done
48 packages can be upgraded. Run 'apt list --upgradable' to see them.<div class="open_grepper_editor" title="Edit &amp; Save To Grepper"></div></pre>
  

<h2>Step 4 — Install ROS Noetic Desktop Full</h2>
<p>Now we are ready to install Noetic on Ubuntu 20.04, To install ros-noetic-desktop-full, run the following:</p>
    
    sudo apt install ros-noetic-desktop-full
    
After you run the command above, Press Y and enter or simply press enter to continue installing.
This whole installation will take about 10 minutes.


<h2> Step 5 - Set up ROS Noetic environment </h2>
<p>After installing ROS Noetic on your Ubuntu 20.04 computer, we will now set up your environment. To do that, run the command below:</p>
    
    source /opt/ros/noetic/setup.bash

<p>To avoid run the command above every time, it is recommended to put it in the .bashrc file located in the home directory ~. To do it run
the following:</p>
    
    echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc

      
  
<h2> Step 6 - Verify Noetic installation </h2>
<p>We can simply run <code>roscd</code> to start a ros master. You can see the current directory of your prompt is changed to where we installed Noetic
<code>/opt/ros/noetic</code>.</p>
