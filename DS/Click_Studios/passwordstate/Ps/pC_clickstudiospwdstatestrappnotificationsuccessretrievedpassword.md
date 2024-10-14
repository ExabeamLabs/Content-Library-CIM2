#### Parser Content
```Java
{
Name = clickstudios-pwdstate-str-app-notification-success-retrievedpassword
  Vendor = Click Studios
  Product = Passwordstate
  TimeFormat = "dd-MM-yyyy HH:mm:ss"
  Conditions = [ """Passwordstate:""", """retrieved the Password record""" ]
  Fields = [
    """({time}\d{2}-\d{2}-\d{4}\s\d{2}:\d{2}:\d{2})\s""",
    """IP Address\s+=\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """\d\d:\d\d:\d\d\s({host}[\w\-.]+)\s+""",
    """Passwordstate:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)?(\s+)""",
    """\s({event_name}retrieved the Password record)""",
    """Passwordstate:\s({full_name}[^\(]+?)\s\((({domain}[^\\\)\s]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\)"""
   ]
   ParserVersion = "v1.0.0"


}
```