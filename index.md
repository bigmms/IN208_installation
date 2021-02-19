# Software Installation Instructions in IN208

This semester, we are standardizing on the following variant of Python: **Anaconda's Python 3.6.x**, where "**x**" can be any number. 

You may have your own computer and wish to install this semester's version of Python on it. Installing Python can be more complicated than using it. We have tried to make installation as simple as possible via step-by-step instructions. It's okay if you don't understand all the steps. Also, these instructions are lengthy because we are trying to support multiple operating systems. In practice, *you should be able to finish the installation in 15-20 minutes*.

If you have problems, and if you have a laptop, the best thing to do is to bring it in to someone to look at. Any of the TAs can help you with this. If you cannot bring in your computer, we have provided you with some diagnostic instructions below. If you are having difficulty with these instructions, feel free to post your questions on Piazza ([Sign up for piazza here](https://piazza.com/yzu.edu.tw/spring2021/in208)) or [reach out to me](https://calendly.com/bhchen/15min?month=2020-02) during my office hour.

# Install Python 

While installing the base Python package is usually straight-forward, getting add-ons for Python can be a bit tricky. That is why we have decided to standardize on the [Anaconda version of Python](https://www.anaconda.com/download/), which is free, quickly becoming standard on many python communities, and contains a lot of add-ons, limiting the number of things you need to install later.

## Install on Windows

We requite that all students with Windows use Windows 10. Even if you have Anaconda installed already, it is safest if you install from the links below to guarantee that you have the correct version for this class.

### Install Anaconda for Python 3.6

1. Use one of the two links below to install the correct version for your operating system. Most modern Window installations are 64-bit. However, if you are unsure, download the 32-bit version. The 32-bit version is guaranteed to work on all systems.

* [Windows 32-bit Anaconda 3.7](https://repo.anaconda.com/archive/Anaconda3-2019.10-Windows-x86.exe)
* [Windows 64-bit Anaconda 3.7](https://repo.anaconda.com/archive/Anaconda3-2019.10-Windows-x86_64.exe)

2. The file that you download is an installer app. Simply double-click on it and follow directions. At some point, you will be asked whether you want to install for yourself or for all users. **Select the option "All Users (requires admin privileges)"**, as shown below.

   ![windows-anaconda-install](imgs\windows-anaconda-install.png)

3. On the next page it will ask you what directory you want to install in. By default, it will install in `C:\ProgramData\Anaconda3`. Leave this alone and click **Next**.

   ![windows-anaconda-directory](imgs\windows-anaconda-directory.png)

4. Finally, you will see a page with checkboxes talking about your Path. **You must select the top box, even though you get a warning not to**. If you do not check this box, you will not be able to use Python from the [PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/overview?view=powershell-7).

   ![windows-anaconda-path](imgs\windows-anaconda-path.png)

### Setup Your Python Environment

The easiest way to start Anaconda command prompt is just type **Anaconda prompt** in your window search option. Once you have anaconda installed, you can follow these steps.

1. Go to the start menu and type in Anaconda Prompt

   ![windows-anaconda-window-search](imgs\windows-anaconda-window-search.png)

2. You should see something like:

   ![](imgs\windows-anaconda-prompt.png)

3. In your Anaconda Prompt, run:

~~~ bash
conda create -n IN208 python=3.6 numpy scipy pip
activate IN208
~~~

4. Once you have finished, you are ready to [install PyCharm](#install-pycharm).

## Install on Macintosh

We have standardized on **Python version 3.6**. The version of Python that we are using for this class is only compatible with Sierra (10.12) or higher. If you have an older version of MacOS, we recommend that you upgrade to Catalina (10.15) immediately.

Even if you have Anaconda installed already, it is safest if you install from the links below to guarantee that you have the correct version for this class.

### Install Anaconda for Python 3.6

1. Use the below to install the correct version for your operating system. The file that you download is an installer app. 

* [ Mac OS X 64-bit Anaconda 3.7](https://repo.anaconda.com/archive/Anaconda3-2019.10-MacOSX-x86_64.pkg)

2. Simply double-click on it and follow directions. You may wish to change the install location on this page:

   ![macos-anaconda-select](imgs\macos-anaconda-select.png)

3. Note that you may see the following error message:

   ![macos-anaconda-error](imgs\macos-anaconda-error.png)

4. This problem is easy to solve. If you just click on the house, it will now look like this.

   ![macos-anaconda-local](imgs\macos-anaconda-local.png)

5. It is okay for you to install Anaconda this way. However, we would prefer that you install it for all users instead. Select the hard drive icon below the house. When you are done, it should look like this.

   ![macos-anaconda-global](imgs\macos-anaconda-global.png)

6. Select the button **Choose Folder** to the right. This will tell it where to put Anaconda. We recommend that you put it in the **Applications** folder.

### Setup Your Python Environment

The easiest way to start Anaconda command prompt is just type **Anaconda prompt** in your window search option. Once you have anaconda installed, you can follow these steps.

1. Open a **new terminal** on your Mac. You can do this by clicking on the Spotlight magnifying glass at the top right of the screen, type **terminal** then click on the terminal icon. Now, type the following command into your terminal

   ![](imgs\macos-anaconda-terminal.png)

2. You should see something like:

   ![](imgs\macos-anaconda-prompt.fw.png)

3. In your terminal window or Anaconda Prompt, run:

~~~ bash
activate
conda create -n IN208 python=3.6 numpy scipy pip
activate IN208
~~~

4. Once this is done, you are ready to [install PyCharm](#install-pycharm).

## Install on Linux

Linux installation is possible, but it is not as straightforward as the two main OS options. In particular, to install on Linux, you have to be comfortable with the appropriate [command shell](http://linuxcommand.org/lc3_lts0010.php) and be ready to install files with a package installer. If this sounds daunting to you, you might want to rethink whether you want to use Linux just yet.

For this class, we require **Python version 3.6**.

### Install Anaconda for Python 3.6

1. Use the below to download the correct version for your operating system. The file that you download is a SH file. 

~~~bash
wget -c "https://repo.anaconda.com/archive/Anaconda3-5.2.0-Linux-x86_64.sh" -O conda.sh 
~~~

2. In your terminal window, run:

~~~bash
bash conda.sh -b
~~~

Follow the prompts on the installer screens. If you are unsure about any setting, accept the defaults. You can change them later.

3. Setup your environment variables, run:

~~~bash
echo 'export PATH=~/anaconda3/bin:${PATH}' >> ~/.profile
source ~/.profile
~~~

### Setup Your Python Environment

1. Just type **Ctrl**+**Alt**+**T** to open a **new terminal** on your Linux.

   ![](imgs\linux-anaconda-terminal.png)

2. In your terminal window or Anaconda Prompt, run:

~~~ bash
source activate
conda create -n IN208 python=3.6 numpy scipy pip
source activate IN208
~~~

3. Once this is done, you are ready to [install PyCharm](#install-pycharm).

# Install PyCharm

Now that you have installed Anaconda, it is a good idea to test the installation out, using the **PyCharm** for your OS. **PyCharm** is an integrated development environment used in computer programming, specifically for the Python language.

It provides code analysis, a graphical debugger, an integrated unit tester, integration with [version control systems](https://en.wikipedia.org/wiki/Revision_control) (VCSes), and supports web development with [Django](https://en.wikipedia.org/wiki/Django_(web_framework)) as well as [Data Science](https://en.wikipedia.org/wiki/Data_science) with [Anaconda](https://en.wikipedia.org/wiki/Anaconda_(Python_distribution)).

PyCharm is [cross-platform](https://en.wikipedia.org/wiki/Cross-platform), with [Windows](https://en.wikipedia.org/wiki/Windows), [macOS](https://en.wikipedia.org/wiki/MacOS) and [Linux](https://en.wikipedia.org/wiki/Linux) versions. The Community Edition is released under the [Apache License](https://en.wikipedia.org/wiki/Apache_License),[[8\]](https://en.wikipedia.org/wiki/PyCharm#cite_note-community-8) and there is also Professional Edition with extra features – released under a [proprietary license](https://en.wikipedia.org/wiki/Proprietary_software).

## Install on Windows

1. Use the below to install the correct version for your operating system. The file that you download is an installer app. 

* [PyCharm Community](https://download-cf.jetbrains.com/python/pycharm-community-2019.3.3.exe)

2. Once your download is complete, navigate to the executable file in the explorer. Run the executable file. 

   ![](imgs\windows-pycharm-install.png)

3. The windows installer for PyCharm is straightforward and intuitive. It is a good idea to associate PyCharm with `.py` files, especially if PyCharm is the primary Python IDE.

   ![](imgs\windows-pycharm-py.png)

4. Mind the following options in the installation wizard

   - **64-bit launcher**: Adds a launching icon to the Desktop.
   - **Open Folder as Project**: Adds an option to the folder context menu that will allow opening the selected directory as a PyCharm project.
   - **.py**: Establishes an association with Python files to open them in PyCharm.
   - **Add launchers dir to the PATH**: Allows running this PyCharm instance from the Console without specifying the path to it.


5. Once this is done, you are now are ready to [test your installation](#test-your-installation).

## Install on Macintosh

1. Use the below to install the correct version for your operating system. The file that you download is an installer app. 

* [PyCharm Community](https://download-cf.jetbrains.com/python/pycharm-community-2019.3.3.dmg)

2. Once the PyCharm installation files has been downloaded, run the program and follow the instructions. Drag the program into applications, and verify the installation as requested. 

   ![](imgs\macos-pycharm-install.png)

3. Select color scheme according to preference. The color scheme may be changed at any time from the “Preferences” menu.

   ![](imgs\macos-pycharm-color.png)

4. Install Featured Plugins During Setup. Some useful plugins are offered during installation. Of these, most users should install Markdown and Bash support. Markdown will allow previewing documentation for Python projects. Vim Keybindings are only helpful for those coming from Vim, while R language is a non-Python language useful in Data Science. These can be installed at any time from “Preferences.”

   ![](imgs\macos-pycharm-plug.png)

5. Once this is done, you are now are ready to [test your installation](#test-your-installation).

## Install on Linux

1. For Ubuntu 16.04 and later, you can use snap packages to install PyCharm. To install the latest stable release of PyCharm, run the following command:

   ``` bash
   sudo snap install pycharm-community --classic
   ```

   ![](imgs\linux-pycharm-terminal.png)

2. Now that PyCharm is installed, you can start it from the **Application Menu** of Ubuntu. Just search for **pycharm** in the **Application Menu** and you should see PyCharm icon as marked in the screenshot below. Just click on it, or run `pycharm-community` in the Terminal.

   ![](imgs\linux-anaconda-config.png)

3. As you’re running PyCharm for the first time, you will have to do some initial configuration. Once you see the following window, click on **Do not import settings** and click on **OK**.

   ![](imgs\linux-anaconda-config2.png)

4. Now, you will see the JetBrains license agreement window. Click on **I confirm that I have read and accept the terms of this User Agreement** and click on **Continue** to accept the license agreement.

   ![](imgs\linux-anaconda-license.png)

5. Select color scheme according to preference. The color scheme may be changed at any time from the “Preferences” menu.

   ![](imgs\linux-anaconda-color.png)

6. Once you select a theme, you can click on **Skip Remaining and Set Defaults** to leave everything else the default and start PyCharm. Otherwise, click on **Next: Featured plugins**. These can be installed at any time from “Preferences.”

   ![](imgs\linux-anaconda-plug.png)

7. Once this is done, you are now are ready to [test your installation](#Test-Your-Installation).

# Test Your Installation

Using the PyCharm requires a bit of practice, so we have created a separate [page of tips and tricks](https://www.jetbrains.com/pycharm/guide/playlists/42/) for this. Right now, all you need to know is how to startup a new project from the PyCharm.

1. The most important step is pointing PyCharm to your Python distribution. In this case, we see the location of python 3.6 from Anaconda. 

   ![](imgs\windows-pycharm-project.png)

2. After the project is created, add a new `.py` file from a folder’s context menu.

   ![](imgs\windows-pycharm-pyfile.fw.png)

3. To get the `.py` file to do something, just type a `print("Hello IN208!")` and hit the Run button. You should see something like:

   ![](imgs\windows-pycharm-in208.png)

4. You have a working installation of Anaconda Python 3.6 + PyCharm on your OS.

# Install PC^2

**PC^2** is the **P**rogramming **C**ontest **C**ontrol System developed at California State University, Sacramento (**CSUS**) in support of Computer Programming Contest activities, and in particular the [International Collegiate Programming Contest (ICPC)](http://icpc.baylor.edu/icpc/) and its Local and Regional Contests around the world.

Because of its success in local and regional programming contests around the world, we are exciting to use the **PC^2** to include IN208. This system will give you immediate feedback while you are waiting on help from a course staff member. In addition, it gives you an opportunity to complete a homework on your own under your account.

## Install JDK for PC^2

The Java Development Kit (JDK), officially named "Java Platform Standard Edition" or "Java SE", is needed for writing Java programs or using programs that were written by Java. The JDK is freely available from Sun Microsystems (now part of Oracle). 

### Install on Windows

1. Uninstall Older Version(s) of JDK. We requite that all students use **Java SE Development Kit 7u80**. Although you can install multiple versions of JDK concurrently, it is messy. Even if you have JDK installed already, it is safest if you install from the links below to guarantee that you have the correct version for this class.

   * [Windows 32-bit JDK-7u80](http://140.138.152.165:5000/sharing/eUQoVLRCO)
   * [Windows 64-bit JDK-7u80](http://140.138.152.165:5000/sharing/PGFHkVQex)

2. Install JDK. Run the downloaded installer (e.g., `jdk-7u80-windows-{x}.exe`), where "**x**" is your OS distribution, and follow the wizard steps.

   ![](imgs\windows-jdk-install.png)

3. Once this is done, you are now are ready to [setup PC^2](#setup-pc2).

### Install on Macintosh

1. Uninstall Older Version(s) of JDK. We requite that all students use **Java SE Development Kit 7u80**. Although you can install multiple versions of JDK concurrently, it is messy. Even if you have JDK installed already, it is safest if you install from the links below to guarantee that you have the correct version for this class.

* [Mac OS X 64-bit JDK-7u80](http://140.138.152.165:5000/sharing/ABuB7yDor)

2. Install JDK. Run the downloaded installer (e.g., `jdk-7u80-macosx-x64.dmg`), and follow the wizard steps.

   ![](imgs\macos-jdk-install.png)

3. Once this is done, you are now are ready to [setup PC^2](#setup-pc2).

### Install on Linux

1. We shall choose the Oracle JDK 7u80. Ubuntu chooses OpenJDK as its default JDK, which is not 100% compatible with Oracle JDK. Check if JDK has already been Installed by opening a Terminal and issue this command:

```bash
javac -version
```

If a JDK version number (e.g., "`javac x.x.x`") appears, JDK has already been installed. You can skip the installation and goto [setuping PC^2](#Setuping-PC^2). To remove OpenJDK, issue command:

```bash
sudo apt-get purge openjdk-\*
```

2. Even if you have JDK installed already, it is safest if you install from the links below to guarantee that you have the correct version for this class.

   * [Linux 32-bit JDK-7u80](http://140.138.152.165:5000/sharing/cjIedgMWu)

   * [Linux 64-bit JDK-7u80](http://140.138.152.165:5000/sharing/rSWMoro4i)

3. The tarball will be downloaded in directory `~/Downloads`, by default. 

   For x64-based OSs, extract the downloaded package by issuing these commands:

```bash   
cd ~/Downloads
gzip -dc jdk-7u80-linux-x64.tar.gz | tar xf -
sudo mkdir /usr/lib/jvm
sudo mv jdk1.7.0_80 /usr/lib/jvm
```

​       For x86-based OSs, extract the downloaded package by issuing these commands:

```bash
cd ~/Downloads
gzip -dc jdk-7u80-linux-i586.tar.gz | tar xf -
sudo mkdir /usr/lib/jvm
sudo mv jdk1.7.0_80 /usr/lib/jvm
```

4. Inform the your Linux to use this JDK:

``` bash
sudo update-alternatives --install "/usr/bin/java" "java" \
    "/usr/lib/jvm/jdk1.7.0_80/bin/java" 1
sudo update-alternatives --install "/usr/bin/javac" "javac" \
    "/usr/lib/jvm/jdk1.7.0_80/bin/javac" 1
sudo update-alternatives --install "/usr/bin/javaws" "javaws" \
    "/usr/lib/jvm/jdk1.7.0_80/bin/javaws" 1
```

5. Use this Oracle JDK as the default:

``` bash
sudo update-alternatives --config java
sudo update-alternatives --config javac
sudo update-alternatives --config javaws
```

6. To verify the JDK installation, issue these commands in step 1. You should see a JDK version number (e.g., "`javac x.x.x`"), if JDK is installed successfully. 

## Setup PC^2

PC^2 is mostly written in Java (using *Eclipse*) and is intended to run on any Java 1.7 (or greater) platform, including Windows, Mac OS X (10.4+) and a variety of Unix-based systems including Solaris, Linux, and FreeBSD.

1. Use the below to install the PC^2 for your operating system. The file that you download is a zip archive. 
   
* [PC^2 v9.5.3](/util/pc2-in208.zip)
   
2. Simply double*-*click on the Zip archive to unzip it. Use your **File Explorer**, navigate to `\pc2-IN208\bin` to run the bat file `pc2team.bat`. You should see a login page like:

   ![](imgs\windows-pc2-login.jpg)

3. To submit your answers, sign in using your PC^2 Account announced in YZU Portal, then select the problem set that wish to answer from the list on the following page and click on `Submit` button. 

   ![](imgs\windows-pc2-problem.jpg)

4. You should see something like this if you answered questions correctly.

   ![](imgs\windows-pc2-yes.jpg)

5. PC^2 will be available starting from the beginning of this semester for all registered students to submit their answers to each problem set; the PC^2's [website](http://140.138.145.204/) will then display which questions have been answered correctly (marked as green boxes). 

   ![](imgs\windows-pc2-website.jpg)

6. Students can submit their answers at any time once the PC^2 has been made available. Generally, however, they should aim to submit their answers for each problem set no later than 1 week after the next problem set becomes available. The final deadline for answer submission will be on the last week of this semester.

# Support or Contact

Having trouble with your setup? Check out our class discussion [here](https://piazza.com/yzu.edu.tw/spring2021/in208) and we’ll help you sort it out.