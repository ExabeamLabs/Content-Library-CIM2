#### Parser Content
```Java
{
Name = cisco-duo-kv-app-login-fail-adminloginerror
  Vendor = Cisco
  Product = Duo Access
  ParserVersion = "v1.0.0"
  TimeFormat = "MM/dd/yyyy HH:mm:ss"
  Conditions = [ """action=admin_login_error;""", """username=""", """description=""" ]
  Fields = [
    """\d\d:\d\d\s+({host}.+?)\s+(\S+\s+)*@\{action=({action}[^;]+)""",
    """timestamp=\s*({time}\d+\/\d+\/\d\d\d\d \d\d:\d\d:\d\d)""",
    """({app}DUO)""",
    """username=({full_name}[^;\}]+)""",
    """username=({first_name}[^;\}\s]+)\s+({last_name}[^;\}]+)""",
    """object=\s*({object}[^;]+?)(?:;|\})""",
    """"email"+:\s*"+({email_address}[^"]+?)"+,""",
    """"ip_address"+:\s*"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"error"+:\s*"+({failure_reason}[^"]+?)"+,""",
  ]


}
```