# linux_basic

## Basic comand 


### About System

`ps` - show processes

`Ctrl+Z`  - отправить процесс на background -  process to background mode

`fg` - return process from background mode

`Ctrl+C`– прекратить процесс вообще - stop process

`uptime`  - время с последнего включения - time from last turn on

`uname` - version Linux 

`user -a` - more info about Linux

`lscpu` – данные процессора - info about processor

`clear` - clean terminal

`ls` - show directory - показать что в этой директории

`ls -l` - more info about directory(with rights)

`ls –la –R  / `   - показать все на компутере - show all files in pc

`exho $PATH` - show directories from wich we use commands

`echo` -show text

`echo Hello!` - show "Hello!"

`ctrl(left) + F3` -switch to linux wihout grafic interface

`ctrl(left) + F4` -switch to linux wihout grafic interface add new session and you can next session ctrl(left) + F5

`alt(left) + F3 or F4` - switch between sessions(tty)

`ctrl(left) + alt + F2` - exit from mode without grafic interface

`man` – помощь - help

`man -k time` -find all avaible commands wich contains word "time"

`man uptime`  - show manual info about command "uptime" . When we in text redactor we can find word `/word` - show all "word" in this manual(to move between "word" use `n`). To exit `q`

`info` – помощь - help documentation 

`info uptime`  - show manual info about command "uptime" . When we in text redactor we can find word `/word` - show all "word" in this manual. To exit `q`

`whatis` – показывает что делает комманда - show short description command

`whatis uptime` – показывает что делает комманда - show short description command "uptime"

`whereis`– показывает где файл -show place of file where command

`whereis uptime` - show file where command

`locate` – показывает где файл - need to install

`locate uptime` - show directory where file or test.txt
  

### Work with directories

`/` - root directory - коренная директория Linux

`/home` - directory where users

`/media` - diks directory

`pwd` – вывести путь где мы сейчас - path to current place where we are

`~ `  - сокращение нашей Home директории - short name home dirrectory when you are in `/home/username`

`..`    - директория которая выше - directory which above current

`. `    - директория где мы сейчас - current directory

`cd`  - сменить директорию - change directory

`cd` or `cd ~` - move to home directory `/home/username`

`cd ~/test/` - move to `/home/username/test/`

`cd /` - move to root directory "/" we can `cd /home`

`cd ..` - move to directory above

`cd ../..` - move to 2 directory above

`ls` – вывести содержимое директории - show all in directory

`ls -l` - more info about directory(with rights)

`ls -la` - show all in directory include hidden

`ls –la –R  / `   - показать все на компутере - show all files in pc

`mkdir` – создать директорию -create directory

`mkdir dir1` -create directory dir1

`mkdir dir1/dir2` - create dir2 in dir1

`mkdir -p dir3/dir4` - create dir3 and dir4 in dir3

`ls -R dir3` -show name dir3: and dir4

`ls -Rla dir3` -show name dir3: and dir4 with hidden

`mv`  - переименовать или перенести директорию

`mv dir1 dirr` - rename dir1 to dirr

`rmdir` – стереть пустую директорию

`rmdir dirr` - remove if dirr empty

`rm –R`   – стереть не пустую директорию со всем что внутри - delete not empty directory

`rm -R  dir*` - remove all directories started "dir"

`cp`     - копировать директорию - copy directory

`cp -R dir2 dir4` - copy directory dir2 to dir4 with all files


`DONT DO IT DANGER!!!`  `sudo rm –R  / --no-preserve-root`   - замочить систему Linux - kill system



### Work with files

`cat` - show file

`cat text.txt` - show file use `Tab` when in directory to autofilling for example `cat t`+Tab == `cat text.txt`

`more text.txt` - show file by pages, to read next use `Enter` to exit `q`.

`less text.txt` - show file  When we in text redactor we can find word `/word` - show all "word" in this manual(to move between "word" use `n`). To exit `q`

`touch` – создать файл или обновить время

`toch test.txt` -create file test.txt if you again use `touch test.txt` will be updated date creation

`cp`  - скопировать файл - copy file

`cp test.txt /home/user/data/` - cp fileName then directory where we want to copy(copy test.txt to /home/user/data/)

`cp t*.* dir` - copy all files started "t" to directory dir

`cp file?.txt -v dir` - file?.txt it mean that any symbol can be instead ? , copy all files according pattern to dir; `-v` mean show what we do 

`cp -R dir newdir` - copy directory dir into directory newdir

`rm` – стереть файл - delete file

`rm *` -delete all files in directory

`rm dir/*` - delete all files in dir

`mv` – перенести файл или переименовать - move or rename file

`mv secret.txt .secret.txt` - make file hidden to show it use `ls -la`

`mv .secret.txt ~/Desktop/` - move secret.txt to desktop directory



### Create Links

`ln`   - создать дубликат файла 

`ln –s `  - создать symbolic линк на файл или директорию типа Shortcut

`ln -s /home/user/dir MyLinkToDir` - create link to directory dir (always use absolute path) with name link MyLinkToDir

`cd MyLinkToDir` - go to dir by link

`mv MyLinkToDir ~/Desktop/` - move link to desktop directory

`ln -s file.txt MyFile` - link to file file.txt (we can create a few links to one file, if we remove file links will be read)

`toch MyFile` - change data creating file.txt

`rm MyFile` - remove link

`ln file.txt fileduplicate` - !!!only for file!!! create duplicate(clone) file.txt with name fileduplicate (if we change file.txt duplicate also change in back order too)


### Commands 

`find` - найти файл - find file

`find /home -name "*.txt"` - find all files .txt in home directory

`find /home -name "file*.txt"` - find all files name starts from file .txt in home directory

`wc`  - вывести количество строк, слов, байт - count quantity of strings(lines), words, bytes

`wc linux.txt` - show quantity in file linux.txt

`wc -l linux.txt` - show quantity only strings in file linux.txt

`wc -w linux.txt` - show quantity words in file linux.txt

`cut` – вывести определенное поле из текста - show field by delimeter

`cut -d ">" -f 3 filedata.txt` - show fild by delimeter ">" 3d column from file filedata.txt

`cut -d ">" -f 3 filedata.txt | sort` - show fild by delimeter ">" 3d column from file filedata.txt then sort them

`sort` – вывести отсортированный текст - show sorted file do not change file

`sort numbers.txt` - show sorted numbers.txt(by char)

`sort -n numbers.txt` - show sorted numbers.txt(by numbers)

#### Grep

`grep`  - поиск определонного слова в файле и вывод строк с этим словом -find words in file and show strings with it

`grep error ./*` - find error in current directory in all files

`grep -i error ./*` - find error in current directory in all files ignore case sensitive

`grep -i error ./* | less` - find error in current directory in all files ignore case sensitive in editor

`grep .com logs.txt` - find ".com" in file logs.txt

`grep -E "[A-Za-z]*@[A-Za-z]*.com" logs.txt` - find by regexp in file logs.txt

`grep -E "(dev.gov|dev.com)" logs.txt` - find by regexp "dev.gov" or "dev.com" in file logs.txt


##### Regular expression / Регулярные Выражения:

`[A-Z]*`  - любое слово из больших букв - any word upper case

`[a-z]*`  - любое слово из строчная букв - any word lower case

`[0-9]*`   - сколько угодно подряд стоящих цифр - any numbers

`\.` - "."

`[A-Za-z]*@[A-Za-z]*.com`   – простое выражение емайлов с окончанием .com  - simple expression with ".com"

`www\.[a-z]*\.com`  - любой вэб адресс  с окончанием .com - any web address with ".com"

### Redirecting IO

`sort names.txt > sorted_names.txt` - sort file names.txt and record to new file sorted_names.txt

`sort -n numbers.txt > sorted_names.txt` - sort by number numbers.txt and rewrite(will be deleted info wich was in file) to sorted_names.txt 

`sort names.txt >> sorted_names.txt` - sort names.txt and add to sorted_names.txt (not rewrite)

`sort names.txt > names.txt` - firstly create file then sort(!!! will be empty )

`sort -n numbers.txt >> numbers.txt` - sort by number numbers.txt and add sorted to numbers.txt

`grep sv /etc/* 2> errors.txt` - find sv in directory /etc/ and subdirectories  if error write to file errors.txt (2> - mean redirect bad responses)

`grep sv /etc/* 2> /dev/null` - find sv in directory /etc/ and subdirectories  if error write to no present device(2> - mean redirect bad responses)

`/dev/null`   - устройство находящиеся - no present device

`grep sv /etc/* > good.txt 2> errors.txt` - find sv in directory /etc/ and subdirectories good response write to good.txt if error write to file errors.txt (2> - mean redirect bad responses)

`grep sv /etc/* > good.txt` - find sv in directory /etc/ and subdirectories good response write to good.txt

`grep sv /etc/* &> results.txt` - find sv in directory /etc/ and subdirectories good and bad response write to results.txt

`2>> errors.txt` - add errors to errors.txt


