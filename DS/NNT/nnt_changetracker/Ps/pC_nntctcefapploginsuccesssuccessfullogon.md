#### Parser Content
```Java
{
Name = nnt-ct-cef-app-login-success-successfullogon
  ParserVersion = v1.0.0
  Vendor = NNT
  Product = NNT ChangeTracker
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """|NNT|ChangeTracker Gen 7|""", """|402|Audit User Admin: Successful Logon|""" ]
  Fields = [
    """rt=({time}\w+\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
    """src=({host}[\w\-.]+)\s""",
    """CEF:([^|]*\|){4}({event_code}\d+)""",
    """CEF:([^|]*\|){5}({event_name}[^|]+)""",
    """msg=({additional_info}[^=]+?)\s*(\w+=|$)""",
    """({app}NNT\|ChangeTracker Gen 7)""",
    """suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s\(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """({auth_type}AD)"""
  ]


}
```