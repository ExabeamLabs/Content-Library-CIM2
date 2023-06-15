#### Parser Content
```Java
{
Name = clickstudios-pwdstate-str-app-logout-success-manuallogoff
  Vendor = Click Studios
  Product = Passwordstate
  TimeFormat = "dd-mm-yyy HH:mm:ss"
  Conditions = [ """Passwordstate:""", """Manual logoff for UserID""" ]
  Fields = [
    """({time}\d{2}-\d{2}-\d{4}\s\d{2}:\d{2}:\d{2})\s""",
    """IP Address\s+=\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """\d\d:\d\d:\d\d\s({host}[\w\-.]+)\s+""",
    """Passwordstate:\s+({event_name}Manual logoff for UserID)\s+""",
    """UserID\s+'(({domain}[^']+)\\)?({user}[^']+)"""
   ]
   ParserVersion = "v1.0.0"


}
```