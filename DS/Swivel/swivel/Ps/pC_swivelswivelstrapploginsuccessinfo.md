#### Parser Content
```Java
{
Name = swivel-swivel-str-app-login-success-info
  Vendor = Swivel
  Product = Swivel
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [""" INFO """, """ PINsafe[""", """]: """, """successful"""]
  Fields = [
    """user[:\s]*({user}[\w\.\-]{1,40}\$?)""",
    """({app}PINsafe)""",
    """\d\d:\d\d:\d\d\s({host}[a-fA-F\d.:]+)""",
    """INFO\s*({additional_info}({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}).+?({result}successful).+?)\.?\s*$""",
  ]
  ParserVersion = v1.0.0


}
```