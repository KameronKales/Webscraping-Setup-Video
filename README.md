# Webscraping Set Up Tutorial

In this tutorial you are going to learn how to set up your computer for python webscraping. We will cover all 3 major operating systems. If you run into any problems you can reach me at kam@glance.ai or my preferred way of communication via Facebook Messenger at http://m.me/kameron.kales

## Table of Contents.

Some of this will not make sense to start. Just trust me :) 

1. Learn to use Terminal/Command Prompt
2. Install Python 2.7
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

*Find Terminal: Navigate to your Applications tab and search for "Terminal" . Open Terminal. Don't lose this tab. You will love the terminal once you learn how to use it.*

* Install NodeJS: https://nodejs.org/en/download/

* Install NPM (Should come with NodeJS, so don't worry too much about this step.)

* Install a text editor (Sublime, vim, emacs -- anything works)

* Install LocalTunnel (https://localtunnel.github.io/www/). Don't run the command to start LocalTunnel, yet!

## Step 2:
* Create the Facebook page you would like to have your bot live on. 
The "create page" option is on the left-hand side of your news feed.

![Creating a FB Page](https://cloud.githubusercontent.com/assets/4122993/20243189/29a01c5e-a91b-11e6-9aad-a047b12a5992.png)

## Step 3:
* Head over to https://github.com/KameronKales/Duke2016, click "Star" & then click "Fork" on the upper right-hand side of the page. This makes your own copy of the repository, so that you have write access. Otherwise, you would have to request permission to add your changes to GitHub. 
If you don't have a GitHub account and don't want to make one, skip the above step.

* Once you've forked the repository, head over to the copy on your GitHub, located at *github.com/[YOUR ACCOUNT USERNAME]/Duke2016.* Press "Clone or Download" and copy the link given.

![clone or download image on GitHub](https://cloud.githubusercontent.com/assets/4122993/20243221/d9c87800-a91c-11e6-83c7-15e498e88703.png)

* Run the following command in the terminal:
```
git clone *YOUR LINK*
```

* Navigate into the cloned folder with ```cd Duke2016-by-Glance```

* Run ```npm install``` in your current folder.

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