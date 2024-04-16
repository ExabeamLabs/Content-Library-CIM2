#### Parser Content
```Java
{
Name = cisco-asa-str-app-authentication-fail-authfailed
  ParserVersion = v1.0.0
  Product = Cisco Adaptive Security Appliance
  Vendor = Cisco
  TimeFormat = "yyyy MMM dd HH:mm:ss"
  Conditions = [ """%AUTHPRIV-3-SYSTEM_MSG""", """pam_aaa:Authentication""", """failed""" ]
  Fields = [
    """({time}\d+ \w+\s+\d+ \d+:\d+:\d+)(\.\w+|)\s\w+:\s+%AUTHPRIV-3-SYSTEM_MSG:""",
    """({event_code}%AUTHPRIV-3-SYSTEM_MSG)""",
    """({event_name}pam_aaa:Authentication failed)""",
    """Authentication failed from\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """({failure_reason}Authentication[^"]+?)\s*"*$"""
  ]


}
```