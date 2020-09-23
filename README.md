<div align="center">

## Dump\_String\_To\_File


</div>

### Description

Dumps a string to a file
 
### More Info
 
strString--string to dump

strFile--file to dump to


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Ian Ippolito \(vWorker\)](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/ian-ippolito-vworker.md)
**Level**          |Unknown
**User Rating**    |4.2 (161 globes from 38 users)
**Compatibility**  |VB 5\.0, VB 6\.0
**Category**       |[Debugging and Error Handling](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/debugging-and-error-handling__1-26.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/ian-ippolito-vworker-dump-string-to-file__1-10/archive/master.zip)





### Source Code

```
Sub Dump_String_To_File (ByVal strString As String, ByVal strFile As String)
  Dim fileFile As Integer
  fileFile = FreeFile
  Open strFile For Output As fileFile
    Write #fileFile, strString
  Close fileFile
  Dim intReturn
  On Error Resume Next
  intReturn = Shell("c:\apps\utility\textpad\txtpad16.exe " & strFile, 1)
  On Error GoTo 0
End Sub
```

