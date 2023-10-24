#### Parser Content
```Java
{
Name = unix-unix-str-process-close-success-procdelete
  Conditions = [ """assh:""", """PROC_Delete""" ]
  ParserVersion = "v1.0.0"

aix-template= {
  Vendor = Unix
  Product = Unix
  TimeFormat = "dd MMM yyyy HH:mm:ss.SSSSSS"
  Fields = [
   """({time}\d\d\s\w\w\w\s\d\d\d\d\s\d\d:\d\d:\d\d\.\d\d\d\d\d\d)""",
   """({host}({dest_host}[\w\-\.]+))\sassh:""",
   """({operation}FILE_\w+)""",
   """({operation}PROC_\w+)""",
   """filename\s+(:|=|)\s+(|(({file_path}[^@"]*\/)?({file_name}[^@"]*)))\s+(FILE_|PROC_)""",
   """(FILE_|PROC_)\w+\s+(|({process_command_line}[^\s]+?))\s+""",
   """\sassh:\s*[^@"]*(FILE_|PROC_)\w+\s*[\w\-\.]+\s*({user}[\w\.\-]{1,40}\$?)""",
  ]
  

}
```