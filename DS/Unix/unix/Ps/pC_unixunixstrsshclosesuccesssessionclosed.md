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
   """user\s({user}.+?)\sfrom\s\[({src_ip}[A-Fa-f:\d.]+)\]""",
   """({event_name}session closed)"""
    ]
 DupFields = ["host->dest_host"]


}
```