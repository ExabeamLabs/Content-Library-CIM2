#### Parser Content
```Java
{
Name = unix-unix-str-ssh-close-success-sessionclosed
 Vendor = Unix
 Product = Unix
 ParserVersion = "v1.0.0"
 TimeFormat = "yyyy-MM-dd HH:mm:ss"
 Conditions = [ """sftp-server[""", """]: """, """: session closed """ ]
 Fields = [
   """\d\d:\d\d:\d\d(\.\S+)? ({host}[^\s]+) sftp-server\[""",
   """user\s({user}.+?)\sfrom\s\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]""",
   """({event_name}session closed)"""
    ]
 DupFields = ["host->dest_host"]


}
```