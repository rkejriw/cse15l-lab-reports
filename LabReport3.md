# Lab Report 3

The `find` command is used to search for files and directories.

For this Lab Report, I will be using 4 command-line options for the command `find`:
1. find -iname
2. find -type
3. find -print
4. find -size +N/-N

## find -iname 

The command-line option `find -iname` is used to search for files and directories with a specifc name but unlike `find -name`, `find -iname` is **not** case sensitive. This is useful becuase we don't have to always keep in mind about lower casing or upper casing while giving in the command.

website citation: [Link](https://www.redhat.com/sysadmin/linux-find-command)

Example 1:
```
[cs15lsp23eh@ieng6-203]:911report:152$ find -iname "C*P*.txt"
./chapter-1.txt
./chapter-10.txt
./chapter-11.txt
./chapter-12.txt
./chapter-13.1.txt
./chapter-13.2.txt
./chapter-13.3.txt
./chapter-13.4.txt
./chapter-13.5.txt
./chapter-2.txt
./chapter-3.txt
./chapter-5.txt
./chapter-6.txt
./chapter-7.txt
./chapter-8.txt
./chapter-9.txt
```
* In Example 1, `find -iname "C*P*.txt"` is searching for all the files ending in `txt` in `911report` that have 'C' and 'P' in them. Here, we can clearly see that `-iname` is not case sensitive as we have given in the command of upper case C and P however `chapter` has lowercased letters.

Example 2:
```
cs15lsp23eh@ieng6-203]:biomed:159$ find -iname "R*7*.txt"
./rr167.txt
./rr171.txt
./rr172.txt
./rr37.txt
./rr73.txt
./rr74.txt
```
* In Example 2, `find -iname "R*7*.txt"` is searching for all the files ending in `txt` in `biomed` that have 'R' and '7' in them.

## find -type 

The command-line option `find -type` is used to search for files and directories based on their type. Thus, `-type` takes in a single character argument which specifies what it needs to search for. In my examples I have used `-type d` which searches for directories and `-type f` which searches for regular files. There are more arguments that can be used such as `l,s,b,c and p`. This is useful when we are tring to locate what a particular file is located in. The directory can help us understand how we can reach that file.

website citation: [Link](https://www.redhat.com/sysadmin/linux-find-command)

Example 1:  
```
[cs15lsp23eh@ieng6-203]:stringsearch-data:174$ find -type d
./.git
./.git/branches
./.git/info
./.git/hooks
./.git/refs
./.git/refs/heads
./.git/refs/tags
./.git/refs/remotes
./.git/refs/remotes/origin
./.git/objects
./.git/objects/pack
./.git/objects/info
./.git/logs
./.git/logs/refs
./.git/logs/refs/remotes
./.git/logs/refs/remotes/origin
./.git/logs/refs/heads
./technical
./technical/911report
./technical/biomed
./technical/government
./technical/government/About_LSC
./technical/government/Alcohol_Problems
./technical/government/Env_Prot_Agen
./technical/government/Gen_Account_Office
./technical/government/Media
./technical/government/Post_Rate_Comm
./technical/plos
```
* In Example 1, `find -type d` searches for all the directories inside `stringsearch-data` which contains `technical` and that contains `911report`, `biomed`, `government` and `plos`.

Example 2:  
```
[cs15lsp23eh@ieng6-203]:Alcohol_Problems:181$ find -type f
./DraftRecom-PDF.txt
./Session2-PDF.txt
./Session3-PDF.txt
./Session4-PDF.txt
```
* In Example 2, `find -type f` is searching for all the files inside `Alcohol_Problems` and thus gives the required output.

## find -print 

The command-line option `find -print` is the default behavior of the `find` command and therefore it does not print anything different. However, it is useful as it can be used when we want to specify other options. `find -print` is basically printing the path names of all the files inside a particular directory.

website citation: [Link](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/)

Example 1: 
```
[cs15lsp23eh@ieng6-203]:Post_Rate_Comm:238$ find -print
./Cohenetal_Cost_Function.txt
./Cohenetal_CreamSkimming.txt
./Cohenetal_DeliveryCost.txt
./Cohenetal_RuralDelivery.txt
./Cohenetal_Scale.txt
./Cohenetal_comparison.txt
./Gleiman_EMASpeech.txt
./Gleiman_gca2000.txt
./Mitchell_6-17-Mit.txt
./Mitchell_RMVancouver.txt
./Mitchell_spyros-first-class.txt
./Redacted_Study.txt
./ReportToCongress2002WEB.txt
./WolakSpeech_usps.txt
```
* In Example 1, `find -print` is printing the path names of all the files inside `Post_Rate_Comm`.

Example 2: 
```
[cs15lsp23eh@ieng6-203]:911report:200$ find -print
./chapter-1.txt
./chapter-10.txt
./chapter-11.txt
./chapter-12.txt
./chapter-13.1.txt
./chapter-13.2.txt
./chapter-13.3.txt
./chapter-13.4.txt
./chapter-13.5.txt
./chapter-2.txt
./chapter-3.txt
./chapter-5.txt
./chapter-6.txt
./chapter-7.txt
./chapter-8.txt
./chapter-9.txt
./preface.txt
```
* In Example 2, `find -print` is printing the path names of all the files inside `911report`.

## find -size +N/-N

The command line `find -size +N` or `find -size -N` is used to search for files that are larger or smaller than a specified size - N. The `+N` option finds files that are larger than N blocks and the `-N` option finds files that are smaller than N blocks. This can be useful when you are trying to find a file with a particular size. One possible case where you could use this is when uploading files; you can use the `-size` option to determine if your file matches the criteria for being uploaded onto a particular website.

website citation: [Link](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/)

Example 1: 
```
[cs15lsp23eh@ieng6-203]:biomed:248$ find -size -25
./1471-2105-3-24.txt
./1471-2156-2-8.txt
./1471-230X-2-17.txt
./1471-2334-3-13.txt
./1471-2350-2-8.txt
./1471-2490-3-2.txt
./1472-6769-1-4.txt
./1477-7819-1-10.txt
./cc973.txt
```
* In Example 1, `find -size -25` is finding all files with size smaller than 25 blocks (where a block is typically 512 bytes) inside `biomed`.

Example 2: 
```
[cs15lsp23eh@ieng6-203]:plos:260$ find -size +60
./pmed.0010028.txt
./pmed.0010036.txt
./pmed.0020018.txt
./pmed.0020045.txt
./pmed.0020059.txt
./pmed.0020073.txt
./pmed.0020103.txt
./pmed.0020182.txt
./pmed.0020246.txt
./pmed.0020249.txt
```
* In Example 2, `find -size +60` is finding all files with size larger than 60 blocks (where a block is typically 512 bytes) inside `plos`.
