#### Parser Content
```Java
{
Name = cisco-duo-kv-app-login-fail-adminloginerror
  Vendor = Cisco
  Product = Duo Access Security
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
    """"ip_address"+:\s*"+({src_ip}[a-fA-F\d.:]+)"""",
    """"error"+:\s*"+({failure_reason}[^"]+?)"+,""",
  ]


}
```