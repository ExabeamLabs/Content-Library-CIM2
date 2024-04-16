#### Parser Content
```Java
{
Name = microsoft-azuremfa-str-user-modify-changed
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Azure MFA
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ pfsvc: User """, """changed User """, """ value """ ]
  Fields = [
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s({host}[^\s]+)\spfsvc:""",
    """pfsvc: User\s+"(({email_address}[^"@]+@[^"\s]+)|(NT AUTHORITY\\SYSTEM|(({domain}[^\\"]+)\\)?({user}[\w\.\-]{1,40}\$?)))"""",
    """pfsvc:\s({additional_info}[^.$]+)."""
    ]


}
```