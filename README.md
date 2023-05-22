# AWS-Basics

**###AWS-CLI**

-- Without creating instances we can perform actions on aws console by using AWS CLI

- Download AWS-CLI from browser
![image](https://github.com/Anusha2710/AWS-Basics/assets/47424821/7c40ec71-c83c-4dd6-9f7b-1862dc37d99e)

- Goto GitBash
> aws version = to check whether aws is installed
![image](https://github.com/Anusha2710/AWS-Basics/assets/47424821/62394e1c-7b1d-42b1-8c74-f8021373ceed)

-- We need to Authenticate with AWS now, For that we need security credentials

- Goto AWS Console- Security credentials
![image](https://github.com/Anusha2710/AWS-Basics/assets/47424821/434fbc40-044e-404d-a431-016c4b1d4503)

- Go down, click oncreate access keys
![image](https://github.com/Anusha2710/AWS-Basics/assets/47424821/108dd17b-bb8d-4c64-b07b-9b4e86456921)

- Now, it is created we got Secret Key & Access key (store it somewhere)
![image](https://github.com/Anusha2710/AWS-Basics/assets/47424821/f5b39512-227a-4789-9a85-fe8bcbae357d)

-- We need to configure aws with credentials

- Goto Gitbash
> aws configure = to configure with aws console
![image](https://github.com/Anusha2710/AWS-Basics/assets/47424821/5c2d7169-6413-4c8b-ab0a-a8f8ec184d08)
- always give region name in region section as eg (ap-south-1), dont provide along with availability zone as eg (ap-south-1a)

-- Lets test by creating S3 buckets

> aws s3 mb anufile = to create file inside s3 bucket
> aws s3 ls = to check list of s3 buckets
![image](https://github.com/Anusha2710/AWS-Basics/assets/47424821/e8dc7f1e-7b66-4fe9-9542-6ad8105d3c38)
- now the file is created
- In this way we can create anything by using AWS CLI

**###Shell-commands**

*purpose of Shell Scripting in DevOps:

- we use it for - Infra maintainance
                - code management (interact with git)
                - configuration management
*Usecase:

- For suppose john is a Devops engineer in Amazon
- We use to look over 10,000 VMs, he need to monitor node health of these VMs
- If any of VM doesn't work properly like, if there's issue with cpu or memeory
- Instead of looking into all VMs individually he will write a Shell script and saves in Git repo
- If any issue happens he will just execute shell script automatically in local machine and finds out he problem
- And if anything goes wrong it automatically sends mail that among 10,000 VMs (10 are suspicious, 5 less memory, 5 less cpu)

1. man Command
> man ls = provides details of any command
![image](https://github.com/Anusha2710/AWS-Basics/assets/47424821/125ca27e-7ee1-456e-a9eb-02d7ab61ea99)

2. pwd command
> pwd = present working directory

3. cd command
> cd anu/ = go inside the directory

> cd / = get out of the directory

4. ls command
> ls -ltr = view reverse output order by date (if its a directory it shows d, remaining all files)

5. touch command
> touch = create empty file

6. vi command
> vi test = create empty file (go inside file, click i for insert, after writing esc and :wq for saving file)

7. cat command
> cat test = view contents in file

8. rm command
> rm test = remove file

9. mkdir command
> mkdir anu = create directory

10. rm -r command
> rm -r = remove directory

11. free command
> free = memory of server
![image](https://github.com/Anusha2710/AWS-Basics/assets/47424821/a5aa0234-d368-4b9c-a76e-3ae8a6607c49)

12. nproc command
> nproc =no. of cpu's
![image](https://github.com/Anusha2710/AWS-Basics/assets/47424821/891bc58d-2797-4c47-807d-c1478d936149)

13. df -h command
> df -h = disk size
![image](https://github.com/Anusha2710/AWS-Basics/assets/47424821/3be1a688-e034-47af-a648-3465c1e8c30e)

14. top command
> top = complete info of server (memory,cpu and all)
![image](https://github.com/Anusha2710/AWS-Basics/assets/47424821/76b2286f-1e3f-46b3-aca3-eb90c46f4019)

-- Lets create a file using shell script now

- create a file 
> vi my-first-shell-script.sh

- go inside the file
#!/bin/bash                 = first line in every file called (shebang)
                              - here 'bash' is executable

                              - we also use bash, dash, sh,ksh
                              - some people use 'sh' which redirects to 'bash' by linking concept

echo" my name is anusha"
![image](https://github.com/Anusha2710/AWS-Basics/assets/47424821/785ca91e-6d25-4134-8eeb-473acd2aa61d)

-- Lets execute the file now
>sh my-first-shell-script.sh  =executed
                              o/p: my name is 
![image](https://github.com/Anusha2710/AWS-Basics/assets/47424821/49562769-a0be-4551-8a9d-0f13e99a1eca)

- we can also execute by using "./" as (./my-first-shell-script.sh)
![image](https://github.com/Anusha2710/AWS-Basics/assets/47424821/be01afea-e62a-4492-a0f0-bcb969baab74)

15. chmod command
- to enable this we need to enable permission
- using "chmod" (user, group, everyone)
                (4- read, 2- write, 1- execute)
                (eg- chmod 444 = we are giving read permission to user,group nd everyone)
- Now, we need to give all permissions in order to use ./
> chmod 777 my-first-shell-script.sh    ( which means 4+2+1=7)
![image](https://github.com/Anusha2710/AWS-Basics/assets/47424821/513fa5ed-bba7-423a-9461-7e5d7c4fa0c5)

16. Shell Script1:
- Now, lets write a shell script to create a folder, and 2 files inside the folder everytime when script is executed, we'll also change permissions of file.
> vi sample-shell-script.sh

#!/bin/bash
# create a folder
mkdir anu

# create 2 files
cd anu
touch firstfile secondfile
![image](https://github.com/Anusha2710/AWS-Basics/assets/47424821/1037f673-8d42-45b3-afd8-679ed98bc718)

- lets give permissions now
> chmod 777 sample-shell-script.sh
![image](https://github.com/Anusha2710/AWS-Basics/assets/47424821/5807ced4-70fd-4ddb-b3c8-3a2cd3c856cd)


