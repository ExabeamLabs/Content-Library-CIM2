#### Parser Content
```Java
{
Name = microsoft-exchange-kv-app-login-fail-imap4
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Microsoft Exchange
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """Imap4""", """Exchange Server""", """,login,""", """"R="""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)(,[^,]*){2},({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({dest_port}\d+),({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+),({user}[\w\.\-\!\#\^\~]{1,40}\$?)(,[^,]*){3},({event_name}[^,]+),""",
    """({app}Exchange Server)""",
    """Msg="({additional_info}[^"]+)""",
    """({event_name}LOGIN ({result}failed))""",
    """Error="+({failure_reason}[^"-]+?)\s*[\-"]""",
  ]
  DupFields = ["event_name->operation"]


}
```