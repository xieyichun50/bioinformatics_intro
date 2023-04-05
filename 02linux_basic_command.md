### Linux Basic Command
<i>Please search online for parameter details!!!</i>
- Login, logout and data transfer 
  - Login
  
    `ssh username@ipaddress`
    - for openstack VM
    
      `ssh -i User1_keypair.pem -J YourAccount@publicIP ubuntu@VM_floatingIP`
      
  - Logout
    
    `logout`
    
  - Data transfer with `scp`
    - from local to remote 
    
      `scp /localPath/file username@ipaddress:/remotePath/file`
    - from remote to local 
    
      `scp username@ipaddress:/remotePath/file /localPath/file`
    - when managing folder, use `scp -r`
    - for openstack VM
    
      `scp -i User1_keypair.pem -J YourAccount@publicIP ubuntu@VM_floatingIP:/remotePath/file /localPath/file`

  - Data transfer with `rsync`
    Manage both folder and file, with timestamp cloned.
    - from local to remote
      
      `rsync -avzP /localPath/file username@ipaddress:/remotePath/file`
    - from remote to local
      
      `rsync -avzP username@ipaddress:/remotePath/file /localPath/file`
- View system status
  - Check the running processes, similar to the "task manager" `top`, `htop`
  - Print the memory usage `free -h`
  - Print the hard disk storage `df -h`
  - Print the disk installation `fdisk -l`
  - Check hard disk performance `hdparm -t /your/filesystem`
  - Check CPU temperature `sensors`
  - Install/update software and package `apt-get install`, `apt-get upgrade`, `apt-get update`
- Manage file and folder
  - Change directory `cd`
  - Check your current location `pwd`
  - Create/make directory `mkdir`
  - List items `ls`
  - Copy file/folder `cp file newfile`, `cp -r folder newfolder`
  - Remove file/folder `rm file`, `rm -r folder`
  - Move file/folder `mv original new`
  - Download online `wget onlinelink`
  - Create a new plain text file `cat > newfile`
  - Print out a file `cat file`
  - Preview a file `less file`, quit with `q`
  - Print the first/last few lines of a file `head file`, `tail file`
  - Look for a specific pattern in a file `grep file`
  - Sort contents in a file `sort file`
  - Unique contents in a file `uniq file`
  - Cut contents in a file `cut file`
  - Replace contents in a file `sed file`
  - Word count `wc file`
  - Do in one line, example
    `grep -w "CDS" test.gff | sed 's/_id ".*"://' | sed 's/transcript_id/\t/' | cut -f1,2,3,4,5,6,7,8,9 | sort -k1 | uniq > test.CDS | wc -l`
  - Edit a file with `vim`
  - Manage file ownership `sudo chown -R newowner.newowner dirname`
  - Work with a superuser `sudo your.command`
- Run a task
  - Run a shell task here `sh test.sh`
  - Run a shell task here with log `sh test.sh > test.log`
  - Run a shell task at the background `nohup sh test.sh > test.log 2>&1 &`
  - Run a perl script `perl test.pl`
  - Run a python script `python test.py`
  - Run a R script `Rscript test.R`
  - Kill a task `kill`
