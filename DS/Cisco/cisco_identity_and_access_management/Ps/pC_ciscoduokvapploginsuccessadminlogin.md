#### Parser Content
```Java
{
Name = cisco-duo-kv-app-login-success-adminlogin
  Vendor = Cisco
  Product = "Cisco Identity and Access Management"
  ParserVersion = "v1.0.0"
  TimeFormat = "MM/dd/yyyy HH:mm:ss"
  Conditions = [ """action=admin_login;""", """username=""", """description=""" ]
  Fields = [
    """\d\d:\d\d\s+({host}.+?)\s+(\S+\s+)*@\{action=({operation}[^;]+)""",
    """timestamp=\s*({time}\d+\/\d+\/\d\d\d\d \d\d:\d\d:\d\d)""",
    """({app}DUO)""",
    """username=({full_name}[^;\}]+)""",
    """username=({first_name}[^;\}\s]+)\s+({last_name}[^;\}]+)""",
    """object=\s*({object}[^;]+?)(?:;|\})""",
    """"email"+:\s*"+({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"+,""",
    """"ip_address"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"primary_auth_method"+:\s*"+({auth_method}[^"]+?)"+,""",
    """"factor"+:\s*"+({factor}[^"]+?)"+,""",
  ]


}
```