#### Parser Content
```Java
{
Name = microsoft-azuremfa-str-app-authentication-validate-oath-code
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Azure MFA
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ pfsvc: """, """|validate_oath_code: user """, """updated authentication result.""", """callStatus = Fallback OATH Code Verified""" ]
  Fields = [
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s({host}[^\s]+)\spfsvc:""",
    """({event_code}validate_oath_code)""",
    """validate_oath_code: user\s+"?(({email_address}[^"@]+@[^"\s]+)|(({domain}[^\\\s]+)\\)?({user}[^\s"]+))""",
    """({event_name}Fallback OATH Code Verified)""",
    """({additional_info}updated authentication result)"""
  ]


}
```