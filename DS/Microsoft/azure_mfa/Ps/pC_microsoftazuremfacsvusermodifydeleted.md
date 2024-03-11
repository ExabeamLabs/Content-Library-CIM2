#### Parser Content
```Java
{
Name = microsoft-azuremfa-csv-user-modify-deleted
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Azure MFA
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """pfsvc: User""", """deleted User Mobile App Device record"""]
  Fields = [
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s({host}[^\s]+)\spfsvc:""",
    """pfsvc: User "({user}[^"]+)""",
    """({event_name}deleted User Mobile App Device record)"""
    ]


}
```