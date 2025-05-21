#### Parser Content
```Java
{
Name = clickstudios-pwdstate-str-app-notification-success-checkfailed
  Vendor = Click Studios
  Product = Passwordstate
  TimeFormat = "dd-MM-yyyy HH:mm:ss"
  Conditions = [ """Passwordstate:""", """A scheduled Account Heartbeat check failed to validated the password for""", """PasswordID =""" ]
  Fields = [
    """({time}\d{2}-\d{2}-\d{4}\s\d{2}:\d{2}:\d{2})\s""",
    """IP Address\s+=\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """\d\d:\d\d:\d\d\s({host}[\w\-.]+)\s+""",
    """Passwordstate:\s+({event_name}A scheduled Account Heartbeat check failed to validated the password)"""
   ]
   ParserVersion = "v1.0.0"


}
```