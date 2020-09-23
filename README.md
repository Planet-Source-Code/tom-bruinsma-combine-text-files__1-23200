<div align="center">

## Combine Text Files


</div>

### Description

I wrote this prgram to augment MRTG (Multi Router Traffic Grapher). Each night i generate new configuration files for all my routers, when that finishes this program combines all the files into one primary configuration file. Please Vote if you like it! :)
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Tom Bruinsma](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/tom-bruinsma.md)
**Level**          |Beginner
**User Rating**    |4.8 (19 globes from 4 users)
**Compatibility**  |VB 4\.0 \(16\-bit\), VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0, VB Script, VBA MS Access
**Category**       |[Files/ File Controls/ Input/ Output](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/files-file-controls-input-output__1-3.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/tom-bruinsma-combine-text-files__1-23200/archive/master.zip)





### Source Code

```
Dim sdir, string1, string2
sdir = Dir("\\hurricane\c$\newrouters\*.cfg")
Open "c:\windows\desktop\mrtgcfg.cfg" For Output As #1
Do While sdir <> ""
 Open "\\hurricane\newrouters\" & sdir For Input As #2
 Do While Not EOF(2)
 Line Input #2, string1
 Print #1, string1
 Loop
 Debug.Print sdir
 Close #2
 sdir = Dir()
Loop
Close #1
```

