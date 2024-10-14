#### Parser Content
```Java
{
Name = microsoft-azuremfa-str-user-modify-success-addednewuser
  Vendor = Microsoft
  Product = Azure MFA
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """pfsvc: """, """User """, """added new user"""]
  Fields = [
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s({host}[^\s]+)\spfsvc:""",
    """User "\[?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\]?"""",
    """added new user "({dest_user}[^"]+)"""",
]
  ParserVersion = "v1.0.0"


}
```