# Bandit 0 
`ssh bandit0@bandit.labs.overthewire.org -p 2220`
## Some helpful tips 
- write access to home directories is disabled so for temporary writing we can use '/tmp/' folder. 
You can create a temporary directory by using the following command `mktemp -d`.

## Solution
We need to find the password for the next level. Once we have logged in, we can type the `ls` command to see the contents of the current directory.
We can see a file titled 'readme'. You can `cat readme` to print the contents of the file into stdout.
Then the contents can be used to ssh into the next level. 

# Bandit 1 
`ssh bandit1@bandit.labs.overthewire.org -p 2220`
## Solution 
The file that stores the password for the next level is called '-'. If you try to `cat -` or `vim -`, you will be using 'stdin'
and not doing what you want to do. To use the cat and vim command, you will have to specify the fullpath of the file i.e. 
`cat ./-`. 

# Bandit 2 
`ssh bandit2@bandit.labs.overthewire.org -p 2220`
## Solution 
