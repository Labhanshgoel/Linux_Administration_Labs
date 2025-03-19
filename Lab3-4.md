# Lab 3 & 4


## Experiment Description
This lab focuses on using Linux manual (`man`) pages, searching for commands related to `ext4`, and utilizing **brace expansion** to generate custom strings efficiently.


## Approach

### 1. Viewing the Manual Page for `gedit`
The `man` command is used to access the manual page for a specific command.

#### Syntax:
man <command_name>


#### Example:
man gedit

#### Explanation:
- Opens the manual page for the `gedit` text editor.


### 2. Searching for Commands Related to `ext4`
The `man -k` command searches for commands associated with a specific keyword.

#### Syntax:

man -k <keyword>


#### Example:

man -k ext4

#### Explanation:
- Searches for commands related to the `ext4` file system.


### 3. Using Brace Expansion
Brace expansion is used to generate strings efficiently.

#### Example 1: Creating a List of Strings

echo file_{A,B,C}.txt

**Output:**

file_A.txt file_B.txt file_C.txt


#### Example 2: Creating a Sequence of Numbers

echo number_{1..5}

**Output:**

number_1 number_2 number_3 number_4 number_5


## Snippets of the Task Performed

### 1. Viewing the `gedit` Manual Page
![gedit_manual_page](https://github.com/user-attachments/assets/e06a5ed5-fc1b-4e65-a119-e8d5a78057ae)



### 2. Searching for Commands Related to `ext4`
![man_command](https://github.com/user-attachments/assets/e0fdd27a-762b-496e-8128-d09295d54ff3)



### 3. Demonstrating Brace Expansion
![Brace_expansion](https://github.com/user-attachments/assets/8bf665ce-b170-48b2-88e2-60d73484264e)


---

## Conclusion
In this lab, we:
- Used the `man` command to view manual pages.
- Searched for commands related to `ext4` using `man -k`.
- Demonstrated the use of **brace expansion** for generating strings.
