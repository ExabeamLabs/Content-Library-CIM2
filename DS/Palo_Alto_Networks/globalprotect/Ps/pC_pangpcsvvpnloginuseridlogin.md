#### Parser Content
```Java
{
Name = pan-gp-csv-vpn-login-useridlogin
  Vendor = Palo Alto Networks
  Product = GlobalProtect
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ParserVersion = v1.0.0
  Conditions = [ """,USERID,login,""" ]
  Fields = [
    """\s(-|({host}[\w\-.]+))\s+\d+,({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+).+?,USERID,login,""",
    """,USERID,login,.+?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),(({domain}[^\\\s,]+)\\+)?({user}[^\\\s,]+)""",
    """({app}active-directory)""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
  ]


}
```