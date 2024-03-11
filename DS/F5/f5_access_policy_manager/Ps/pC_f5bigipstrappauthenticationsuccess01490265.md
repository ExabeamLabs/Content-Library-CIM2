#### Parser Content
```Java
{
Name = f5-bigip-str-app-authentication-success-01490265
  ParserVersion = v1.0.0
  Vendor = F5
  Product = F5 Access Policy Manager
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """01490265""", """ BIG-IP """, """have received SAML Assertion from IdP""" ]
  Fields = [
    """:\d\d:\d\d ({host}[\w.-]+)\s""",
    """value \(({user}[^\)]+?)\)""",
    """({app}BIG-IP)""",
    """({event_name}received SAML Assertion from IdP)""",
    """({event_code}01490265)""",
    """({auth_method}SAML)""",
    """({additional_info}BIG-IP[^"]+?)\s*$"""
  ]


}
```