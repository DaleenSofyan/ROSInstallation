<h1 class="entry-title">Installing ROS (desktop-full) Step by Step</h1>

<p>After setting up Ubuntu 20.04 ver on your Virtualbox, follow these steps to install ROS successfully:</p>


<h2 id="1-set-up-ros-noetic-repo-on-ubuntu-2004-"><span class="ez-toc-section" id="Step_1_%E2%80%94_Set_up_ROS_Noetic_repo_for_Ubuntu_20_04"></span>Step 1 — Set up ROS Noetic repo for Ubuntu 20.04<span class="ez-toc-section-end"></span></h2>

<p>To install Noetic on Ubuntu 20.04, first we will need to add the official ROS Noetic repo to <code>sources.list</code>.

![Set up ROS Noetic repo for Ubuntu 20.04](https://github.com/DaleenSofyan/ROSInstallation/blob/main/Images/01.png)


<h2 id="2-add-official-ros-noetic-keyring-on-ubuntu-2004"><span class="ez-toc-section" id="Step_2_%E2%80%94_Add_official_ROS_keyring"></span>Step 2 — Add official ROS keyring<span class="ez-toc-section-end"></span></h2>

<p>
Next, we will need to add the ROS Noetic keyring to get authenticated ROS packages to install on your Ubuntu, There are two ways to add the official key, and you can choose any of them.

The first is to use apt-key to add the key to be downloaded from the Ubuntu key server. by writing the command below:

![Set up ROS Noetic repo for Ubuntu 20.04](https://github.com/DaleenSofyan/ROSInstallation/blob/main/Images/02.png)


The second way is to use curl to download the official ROS key and add it locally. To do this paste the command below:

![Set up ROS Noetic repo for Ubuntu 20.04](https://github.com/DaleenSofyan/ROSInstallation/blob/main/Images/03.png)
</p>


<h2 id="3-update-ros-package-index"><span class="ez-toc-section" id="Step_3_%E2%80%94_Update_ROS_package_index"></span>Step 3 — Update ROS package index<span class="ez-toc-section-end"></span></h2>

<p>
Next, we will need to get the ROS Noetic package information from the repository we just added using apt update, by writing this command:

![Set up ROS Noetic repo for Ubuntu 20.04](https://github.com/DaleenSofyan/ROSInstallation/blob/main/Images/04.png)
</p>

<h2 id="4-install-ros-noetic-on-ubuntu-2004"><span class="ez-toc-section" id="Step_4_%E2%80%94_Install_ROS_Noetic_Desktop-Full"></span>Step 4 — Install ROS Noetic Desktop Full<span class="ez-toc-section-end"></span></h2>

<p>
Now we are ready to install Noetic on Ubuntu 20.04, To install ros-noetic-desktop-full, run the following: 
</p>

![Set up ROS Noetic repo for Ubuntu 20.04](https://github.com/DaleenSofyan/ROSInstallation/blob/main/Images/05.png)


<h2 id="9-set-up-ros-noetic-environment-on-ubuntu-2004"><span class="ez-toc-section" id="Set_up_ROS_Noetic_environment"></span>Set up ROS Noetic environment<span class="ez-toc-section-end"></span></h2>

<p>
After installing ROS Noetic on your Ubuntu 20.04 computer, we will now set up your environment. To do that, run the command below:
</p>

![Set up ROS Noetic repo for Ubuntu 20.04](https://github.com/DaleenSofyan/ROSInstallation/blob/main/Images/06.png)

To avoid run the command above every time, it is recommended to put it in the .bashrc file located in the home directory ~. To do it run the following:

![Set up ROS Noetic repo for Ubuntu 20.04](https://github.com/DaleenSofyan/ROSInstallation/blob/main/Images/07.png)


<h2 id="9-set-up-ros-noetic-environment-on-ubuntu-2004"><span class="ez-toc-section" id="Verify_Noetic_installation"></span>Verify_Noetic_installation<span class="ez-toc-section-end"></span></h2>

<p>
<p>We can simply run <code>roscd</code>. You can see the current directory of your prompt is changed to where we installed Noetic: <code>/opt/ros/noetic</code>.</p>
</p>
