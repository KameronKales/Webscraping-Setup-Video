# Webscraping Set Up Tutorial

In this tutorial you are going to learn how to set up your computer for python webscraping. We will cover all 3 major operating systems. If you run into any problems you can reach me at kam@glance.ai or my preferred way of communication via Facebook Messenger at http://m.me/kameron.kales

## Table of Contents.

Some of this will not make sense to start. Just trust me :) 

1. Learn to use Terminal/Command Prompt
2. Install XCode
3. Install Python 2.7
2. Install Text Editor (Sublime)
3. Install PIP
4. Install GIT
5. Register for a GitHub Account
6. Clone a repository
7. Start scraping!

### Mac OS:
The following instructions will only work for Mac. 

## Step 1: Learn to use Command Prompt/Terminal
The command prompt/terminal is the best way to get your computer to do what you want. On Mac, it is called terminal. On Windows, it is called Command Prompt. They are the same thing. 

Find Terminal-

Navigate to your Applications tab and search for "Terminal" . Open Terminal. Don't lose this tab. You will love the terminal once you learn how to use it.

If you are feeling adventurous I would strongly recommend installing iterm2. It will replace your terminal and adds a lot of great features like copy and paste among others. Here is the link to install. 

Download [HERE](https://www.iterm2.com/)

## Step 2: Install XCode from App Store
This is mandatory. There is no way to progress without completing this step. It is also possible you will need to update your OS with Apple prior to completing this step. If so, plug your laptop in and go to sleep. That will take awhile.

* Navigate to App Store on your Mac

* Search XCode

* Install.

## Step 3: Install Python 2.7
Python might already be installed on your machine. To check this we are going to use the terminal. So, hopefully you still know where it is :)

* Navigate to Terminal

* Type python into the terminal. You should get a result like this. 

![Python Interpreter](/pictures/check_python_version_on_mac.png)

You can tell which version of python you have by the top line. I have python 2.7.10. As long as you have 2.7 something everything will work :)

* If your terminal does not respond in this way, it most likely means you do not have python installed. Let's fix that.

* Run the following code in your terminal. Run each snippet by itself. Do not copy and paste all 4 into your terminal and hit enter. Copy and paste each one individually and hit enter to run it.

``ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
``

``brew doctor
``

``brew update
``

``brew install python
``

## Step 4: Install Text Editor (Sublime)
Navigate to ![Sublime](https://www.sublimetext.com/3) to download. Click the OS X Button shown below.

![Sublime](/pictures/os_x_sublime.png)

* Navigate to your downloads and double click the Sublime Text Build 31....dmg file to open and install it. After it installs, I recommend moving the download to your Applications folder. 


## Step 4: Install PIP
It is possible while doing this step you will see errors. If that happens please add sudo to the front of the command below.

* Type the following command in your command prompt.

``easy_install pip
``

* If you run into this error, please run this line of code instead 

``sudo easy_install pip
``

## Step 5: Install GIT
Is is possible GIT is already installed on your computer. We will check prior to reinstalling. 

Run this code in your command prompt to check if you have GIT

``git --version
``

If you see a version number printed out, you can progress onto Step 6. If you do not, continue below.

``brew install git
``

## Step 6: Register for a Github Account
Registering for a github account is incredibly useful. For the purpose of this video series alone, it will make your life 100x easier. 

Navigate to ![Github](http://github.com)

Complete the sign up form shown below and confirm your email. 

![Github](/pictures/github.png)

Using Github enables you to store your code much like you store files with Google Drive. It also enables you to easily copy the code I write and run it in the same way I wrote it. 

You should choose the free account for our purposes. You will not need the additional features of a paid account. 

Answer the basic questions after declining the paid account and navigate to your profile page. The top right corner has an icon to click and dropdown a menu to view your profile. 

![Profile](/pictures/gitub_account.png)

## Step 7: Clone a Repository
Cloning a repository means to make a copy of it and bring it onto your computer to use. 

* Navigate to your terminal and type CD

* Next, type mkdir Projects

* Next, type CD Projects to switch into the projects folder. 

* Now, we are going to clone the repository.

* Click ![HERE](https://github.com/KameronKales/Sourcers-Who-Code-Scraping-Tutorial-by-Glance) to open the repo.

* Find the green clone or download button on the right. You can check below for a screenshot example.

![Repo](/pictures/github_clone_repo.png)

* Click the green button and copy the url in the clone with git box. You can check below for a screenshot example.

![Git Clone](/pictures/github_clone_repo.png)

* Once you've forked the repository, head over to the copy on your GitHub, located at *github.com/[YOUR ACCOUNT USERNAME]/Duke2016.* Press "Clone or Download" and copy the link given.

![clone or download image on GitHub](https://cloud.githubusercontent.com/assets/4122993/20243221/d9c87800-a91c-11e6-83c7-15e498e88703.png)

* Run the following command in the terminal:
``
git clone *YOUR LINK*
``

* Navigate into the cloned folder with ```cd Duke2016-by-Glance```

* Run ``npm install`` in your current folder.

## Step 4
* Go to https://developers.facebook.com/. Click "Products" in the upper navigation tab, then "Messenger Platform" which is listed under the "Growth and Engagement" tab.

![messenger platform screenshot](https://cloud.githubusercontent.com/assets/4122993/20243246/b6169148-a91d-11e6-8be8-e6c40569ab36.png)

* Then, press the "Start Building" button. You will be directed to a new page. In the top right, there's a dropdown menu called "My Apps." Hover or click and select "Add App" or "Create App" -- either works.

![my apps hover button](https://cloud.githubusercontent.com/assets/4122993/20243256/026ac91a-a91e-11e6-919d-5077699f709d.png)

* A popup will appear. Fill in your app's name and category, then select Create App ID.

* You will be directed to a page called "Product Setup." Select "Messenger" from this list of products (note that "Messenger" and "Messenger Expression" are different -- select "Messenger"!)

* On the "Messenger" page, scroll down to generate a token for your page.

![token generation](https://cloud.githubusercontent.com/assets/4122993/20243276/30b3e378-a91f-11e6-9b1e-d30c96a1c425.png)

* Finally, add this generated token to your ```facebook_bot.js``` file via your text editor.

## Step 5
* Back on the Product Setup page, add "Webhooks" to your app.

* In the popup, leave "Callback URL" blank for now. Your "Verify Token" may be anything you like (don't use any password you've ever used). As for "Subscription Fields," select every "Messenger"-related option.

* In your ```facebook_bot.js``` file, add the "Verify Token" you used to the "verify_token" field.

## Step 6
* Open a new terminal. In your new terminal window, enter the command
```lt --port 5000```

* Copy the resulting URL.

* Enter the URL back on the Webhooks Callback URL. **NOTE** that you need to modify the URL in two places: First, add an "s" to the "http://" so that it reads "https://". Second, add "/facebook/receive" to the end of the URL.

* Press "Verify and Save."

## Step 7
* Return to your original terminal. Enter the command ```node facebook_bot.js```

## Step 8
* You're done! Go to the Facebook page you set up and send it the message, "Hello"!