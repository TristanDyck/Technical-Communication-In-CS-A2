---
layout: post
title:  "README"
date:   2022-11-01 16:59:54 -0500
categories: jekyll update
permalink: /README
---

# Hosting a Resume On GitHub Pages

## Purpose

This document will explain the process and advantages (according to Andrew Etter's *Modern Technical Writing: An Introduction To Software*) of hosting a resume created with Markdown on GitHub Pages.

## Prerequisites
* A resume formatted in Markdown
* A GitHub account
* Have Jekyll installed on your device

## Instructions

### Starting the Website

As covered in the "Make Static Websites" section, it is important that more time is spent on researching, learning, and writing, instead of worrying about site maintenance or software crashes.  For that reason, GitHub Pages is a helpful tool for those who want a stable way to share their resume which requires minimal work to setup.

1. With Jekyll installed, start by navigating to a desirable folder to store your website's project in and put the command,

    ```
    jekyll new [NAME OF WEBSITE]
    ```

    into the terminal.  Exactly what you call the website is up to you, it could just be "Resume," but remember it is a command so there should not be whitespace in the name.  

2. Now you will want to open to the folder itself with the terminal, so enter the command,

    ```
    cd [NAME OF WEBSITE]
    ```

3. We can finally generate the website, simply enter the command,

    ```
    bundle exec jekyll serve
    ```

    into the terminal.  To view the site, look at the line that says "Server address" from the block of text that was entered into the terminal after the last command, and note the number after the last colon at the end of the line (in my case it is 4000).  Open your preferred web browser and enter into the address line, 

    ```
    localhost:[NUMBER]
    ```

    You should now see the default website.

4. If you open the ```_config.yml``` file you will find various placeholder values in title, email, etc.  You should fix these so that they display your own information (such as [YOUR NAME]'s Resume, your email).  You may also delete the default post in the ```_posts``` folder, though reading it first might be informative.  Similarly, you may remove the ```about.markdown``` file.

You now have the start of the website that will soon host your resume!

### Hosting your resume

Using a one-stop-shop for your resume allows you to have greater control over how it is viewed at all times, and for you to continuously update it.  It also offers the opportunity to display some Markdown knowledge and general technical literacy.

1. Navigate to the ```_posts``` folder and insert your resume's markdown file.  Rename it so that it follows a format similar to ```2022-11-01-Resume.md```, replacing the date with the current one of course.

2. Create a repository in GitHub, do not auto-generate a README file.

3. Take whatever you named your GitHub repository (keeping in mind that spaces become dashes) and change ```baseurl``` in ```_config.yml``` to the name of your repository.

4. Go into your resume.md file and add the line ```permalink: /Resume/``` if you would like the resume to be clickable on the top-right corner from anywhere.

5. You will now want to transfer all of the documents in your website's folder to the repository.  There are multiple ways to do this, either using Git locally through your terminal or by manually uploading them in GitHub itself.  If you do the latter, ensure that the file structure is preserved.

6. Now, navigate to ```https://tristandyck.github.io/Technical-Communication-In-CS-A2/``` but replace my username and document name with your own.  You should see your website as well as your resume!

### More Resources

## Authors and Acknowledgements 

 * Andrew Etter' for his *Modern Technical Writing: An Introduction To Software*
 * My group members: Aneesh Makkar, Asifur Rahman, and Katrina Dotzlaw
 * Jekyll for their website template

## FAQs

### Why is Markdown better than a word processor?

Markdown offers more specific control than many word processors, is fairly simple, and allows you to show off a valuable technical skill.

### Why is my resume not showing up?

You may not have followed the naming convention properly.  Check that it is formatted as "YYYY-MM-DD-NAME.md".
