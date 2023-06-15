#### Parser Content
```Java
{
Name = clickstudios-pwdstate-str-app-logout-success-autologoff
  Vendor = Click Studios
  Product = Passwordstate
  TimeFormat = "dd-mm-yyy HH:mm:ss"
  Conditions = [ """Passwordstate:""", """Automatic logoff for user from the IP Address""" ]
  Fields = [
    """({time}\d{2}-\d{2}-\d{4}\s\d{2}:\d{2}:\d{2})\s""",
    """IP Address\s+=\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """\d\d:\d\d:\d\d\s({host}[\w\-.]+)\s+""",
    """msg=({event_name}Automatic logoff for user from the IP Address)""",
   ]
   ParserVersion = "v1.0.0"


}
```