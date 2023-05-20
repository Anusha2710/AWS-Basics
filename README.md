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

> man ls = provides details of any command

> pwd = present working directory

> cd bundle/ = go inside the directory

> cd / = get out of the directory

> ls -ltr = view reverse output order by date (if its a directory it shows d, remaining all files)

> touch = create empty file

> vi test = create empty file (go inside file, click i for insert, after writing esc and :wq! for saving file)

> cat test = view contents in file

> rm test = remove file

> mkdir anu = create directory

> rm -r = remove directory

> free = memory of server

> nproc =no. of cpu's

> df -h = disk size

> top = complete info of server (memory,cpu and all)

-- Lets create a file using shell script now

- create a file 
> vi my-first-shell-script.sh

- go inside the file
> #!/bin/bash                 = first line in every file called (shebang)
                              - here 'bash' is executable

                              - we also use bash, dash, sh,ksh
                              - some people use 'sh' which redirects to 'bash' by linking concept

> echo" my name is anusha"

-- Lets execute the file now
>sh my-first-shell-script.sh  =executed
                              o/p: my name is 
