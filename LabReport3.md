# Lab Report 3

The `find` command is used to search for files and directories.

For this Lab Report, I will be using 4 command-line options for the command **find**:
1. find -iname
2. find -type
3. find -print
4. find -size +N/-N

## find -iname 
* 
example 1:
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
example 2:
```
cs15lsp23eh@ieng6-203]:biomed:159$ find -iname "R*7*.txt"
./rr167.txt
./rr171.txt
./rr172.txt
./rr37.txt
./rr73.txt
./rr74.txt
```
-type 

example 1: finding directory 
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
example 2: finding file 
```
[cs15lsp23eh@ieng6-203]:Alcohol_Problems:181$ find -type f
./DraftRecom-PDF.txt
./Session2-PDF.txt
./Session3-PDF.txt
./Session4-PDF.txt
```
-print 

example 1 : printing all files inside government inside Post_Rate_Comm
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
example 2: printing the path names of all files inside 911report
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
-size +N/-N
example 1: finding files with size lesser than 25 blocks (where a block is typically 512 bytes).
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
example 2: finding files with size bigger than 60 blocks (where a block is typically 512 bytes).
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
