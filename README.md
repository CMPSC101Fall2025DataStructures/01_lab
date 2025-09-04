# CS101 Fall 2025: Lab 01

Building a squaring application and a word search application using Python and the UV package manager.

This repository contains the starter code and instructions for Lab 01 of CS101. The lab focuses on creating a command-line application to search for words in text files.

## Assigned and Due

- __Assigned__: Wednesday, 4 Sept 2025 at 2:35pm
- __Due__: Wednesday 11 Sept 2025 at 2:35pm
- __Expiration__: Wednesday, 18 Sept 2025 at 2:35pm
Note: the *expiration* date is the last date you can submit your work for a grade.

---

![Haiku logo](graphics/haiku_i.png)

You are invited to complete a program to search for words in a body of text.

## Project Goals

We will be working with a package manager called UV to create a Python environment where you will run code. You will also be using a code editor such as VS Code and using the terminal to enter commands to run your code.

As you enhance your technical programming skills, you will find programming with tools such as UV and VS Code to be very helpful to your effort.

This lab assignment also invites you to combine what you learned about the basics of Python programming to implement two small but useful programs. One program loads values to display as squared values, and the other loads a text file to allow for parsing and searching.

## Project Access

You can access this assignment by clicking the link provided to you in Discord or in a course schedule. Once you click this link it will create a GitHub repository that you can clone to your computer by using the `git clone <your-github-repository` command to download the project from GitHub to your computer where you are to work. Now you are ready to add source code and documentation to the project.

## Instructions

You will complete this lab assignment by following two tutorials in order. The first tutorial will guide you through setting up a Python environment using the UV package manager and creating a simple application to read integers from a CSV file and print their squared values. The second tutorial will walk you through creating a word search application that reads a text file and searches for a specified word, printing the lines where the word is found.

1. [Tutorial 1: Setting Up a Python Environment with UV](tutorial_01.md)
2. [Tutorial 2: Creating a Word Search Application](tutorial_02.md)

## Deliverable

Once you have completed the tutorials, please complete your writing accessment at `writing/reflection.md`. 

As you work, please periodically commit your changes and push them to your GitHub repository. This will ensure that your work is saved and can be reviewed by your instructor.

Writing assignment: [Reflections](writing/reflection.md)

## Project Reflection

Once you have finished both of the previous technical tasks, you can use a text editor to answer all of the questions in the `writing/reflection.md` file. For instance, you should provide the output of the Python program in a fenced code block, explain the meaning of the Python source code segments that you implemented, and answer all of the other questions about your experiences in completing this project.

## Submission 

As you are working on your lab, you are to commit and push regularly. The commands are the following.

 ``` bash
git add -A
git commit -m ``Your notes about commit here''
git push
```

After you have pushed your work to your repository, please visit the repository at the GitHub website (you may have to log-in using your browser) to verify that your files were correctly sent.

## Project Assessment

The grade that a student receives on this assignment will have the following components.

- **GitHub Actions CI Build Status [up to 25%]:**: For the lab repository associated with this assignment students will receive a checkmark grade if their last before-the-deadline build passes. This is only checking some baseline writing and commit requirements as well as correct running of the program. An additional reduction will given if the commit log shows a cluster of commits at the end clearly used just to pass this requirement. An addition reduction will also be given if there is no commit during lab work times. All other requirements are evaluated manually.

- **Mastery of Technical Writing [up to 50%]:**: Students will also receive a checkmark grade when the responses to the writing questions presented in the `reflection.md` reveal a proficiency of both writing skills and technical knowledge. To receive a checkmark grade, the submitted writing should have correct spelling, grammar, and punctuation in addition to following the rules of Markdown and providing conceptually and technically accurate answers.

- **Mastery of Technical Knowledge and Skills [up to 25%]**: Students will receive a portion of their assignment grade when their program implementation reveals that they have mastered all of the technical knowledge and skills developed during the completion of this assignment. As a part of this grade, the instructor will assess aspects of the programming including, but not limited to, the completeness and the correctness of the program and the use of effective source code comments.

---

## GatorGrade

### Checks for GatorGrade

For immediate feedback on submissions, we will be using Gator Grade to inform the of missing components in the submission. As you submit, you will notice that there is a thick red X that will change to a green check mark when all components have been included in the submission. You are encouraged to click on the red X to find a listing of the components to address.

You can check the baseline writing and commit requirements for this lab assignment by running department's assignment checking `gatorgrade` tool. To use `gatorgrade`, you first need to make sure you have Python3 installed (type `python --version` to check). If you do not have Python installed, please see:

- [Setting Up Python on Windows](https://realpython.com/lessons/python-windows-setup/)
- [Python 3 Installation and Setup Guide](https://realpython.com/installing-python/)
- [How to Install Python 3 and Set Up a Local Programming Environment on Windows 10](https://www.digitalocean.com/community/tutorials/how-to-install-python-3-and-set-up-a-local-programming-environment-on-windows-10)

Then, if you have not done so already, you need to install `gatorgrade`:

- First, [install `pipx`](https://pypa.github.io/pipx/installation/)
- Then, install `gatorgrade` with `pipx install gatorgrade`

Finally, you can run `gatorgrade`: `gatorgrade --config config/gatorgrade.yml`

## Seeking Assistance

* Extra resources for using markdown include;
  + [Markdown Tidbits](https://www.youtube.com/watch?v=cdJEUAy5IyA)
  + [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
* Do not forget to use the above git commands to push your work to the cloud for the instructor to grade your assignment. You can go to your GitHub repository using your browser to verify that your files have been submitted. Please see the TL’s or the instructor if you have any questions about assignment submission.

Students who have questions about this project outside of the lab time are invited to ask them in the course's Discord channel or during instructor's or TL's office hours.
