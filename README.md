# AWS-Basics

**###AWS-CLI**

-- Without creating instances we can perform actions on aws console by using AWS CLI
- Download AWS-CLI from browser
- Goto GitBash
> aws version = to check whether aws is installed

-- We need to Authenticate with AWS now, For that we need security credentials
- Goto AWS Console- Security credentials- create access keys
- Now, we got Secret Key & Access key (store it somewhere)

-- We need to configure aws with credentials
- Goto Gitbash
> aws configure = to configure with aws console

-- Lets test by creating S3 buckets
> aws s3 mb anufile = to create file inside s3 bucket
> aws s3 ls = to check list of s3 buckets


**###Shell-commands**

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
