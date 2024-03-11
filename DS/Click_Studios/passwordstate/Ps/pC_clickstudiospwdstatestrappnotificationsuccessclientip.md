#### Parser Content
```Java
{
Name = clickstudios-pwdstate-str-app-notification-success-clientip
  Vendor = Click Studios
  Product = Passwordstate
  TimeFormat = "dd-mm-yyy HH:mm:ss"
  Conditions = [ """Passwordstate:""",  """Client IP Address =""" ]
  Fields = [
    """({time}\d{2}-\d{2}-\d{4}\s\d{2}:\d{2}:\d{2})\s""",
    """IP Address\s+=\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """\d\d:\d\d:\d\d\s({host}[\w\-.]+)\s+""",
    """Passwordstate:\s({additional_info}[^:]+?)\sClient IP Address""",
    """UserName\s*=\s*(({domain}[^\\\)\s]+)\\+)?({user}[^\)\s]+)\)"""
   ]
   ParserVersion = "v1.0.0"


}
```