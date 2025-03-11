#### Parser Content
```Java
{
Name = unix-unix-str-process-create-success-proccreate
  Conditions = [ """assh:""", """PROC_Create""" ]
  ParserVersion = "v1.0.0"

aix-template-dl= {
  Vendor = Unix
  Product = Unix
  TimeFormat = "dd MMM yyyy HH:mm:ss.SSSSSS"
  Fields = [
   """({time}\d\d\s\w\w\w\s\d\d\d\d\s\d\d:\d\d:\d\d\.\d\d\d\d\d\d)""",
   """({host}[\w\-\.]+)\sassh:""",
   """({operation}FILE_\w+)""",
   """({operation}PROC_\w+)""",
   """filename\s+(:|=|)\s+(|(({file_path}[^@"]*\/)?(null|({file_name}[^@"]*))))\s+(FILE_|PROC_)""",
   """(FILE_|PROC_)\w+\s+(|({process_command_line}[^\s]+?))\s+""",
   """\sassh:\s*[^@"]*(FILE_|PROC_)\w+\s*[\w\-\.]+\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
  ]
   DupFields = ["host->dest_host"
}
```