#### Parser Content
```Java
{
Name = microsoft-azuremfa-user-delete-deleted
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Azure MFA
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """pfsvc: User""", """deleted user record"""]
  Fields = [
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s({host}[^\s]+)\spfsvc:""",
    """pfsvc: User "({user}[^"]+)""",
    """({event_name}deleted user record) "(({dest_user}[^"@]+@[^"\s]+)|(NT AUTHORITY\\SYSTEM|(({domain}[^\\"]+)\\)?({user}[^\s"]+)))"""
  ]


}
```