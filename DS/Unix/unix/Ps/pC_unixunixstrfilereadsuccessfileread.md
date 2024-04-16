#### Parser Content
```Java
{
Name = unix-unix-str-file-read-success-fileread
 ParserVersion = "v1.0.0"
  Conditions = [ """assh:""", """FILE_Read""" ]

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
unixauditd-str-template= {
  Vendor = Unix
  Product = Unix Auditd
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """\d\d:\d\d:\d\d(\.\S+)?\s({host}[^\s]+)""",
    """USER\s*({user}[\w\.\-]{1,40}\$?)""",
    """(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}[\w\-.]+))\[({=src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\]\)""",
  
}
```