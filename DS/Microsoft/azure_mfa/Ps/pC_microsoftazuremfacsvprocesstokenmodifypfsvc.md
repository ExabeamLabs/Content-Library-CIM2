#### Parser Content
```Java
{
Name = microsoft-azuremfa-csv-process-token-modify-pfsvc
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Azure MFA
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """pfsvc: User""", """changed OATH Token""", """value"""]
  Fields = [
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s({host}[^\s]+)\spfsvc:""",
    """pfsvc: User "({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """({event_name}changed OATH Token)"""
  ]


}
```