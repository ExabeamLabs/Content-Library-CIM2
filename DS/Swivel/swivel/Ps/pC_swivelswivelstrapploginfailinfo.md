#### Parser Content
```Java
{
Name = swivel-swivel-str-app-login-fail-info
  Vendor = Swivel
  Product = Swivel
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [""" INFO """, """ PINsafe[""", """]: """, """failed"""]
  Fields = [
    """user[:\s]*({user}[^\s.,]+)""",
    """({app}PINsafe)""",
    """\d\d:\d\d:\d\d\s({host}[a-fA-F\d.:]+)""",
    """INFO\s*(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}).+?({result}failed)[^"]+)""",
    """error:\s({failure_reason}.+?)\s*$""",
  ]
  ParserVersion = v1.0.0


}
```