#### Parser Content
```Java
{
Name = pan-gp-csv-vpn-login-useridlogin
  Vendor = Palo Alto Networks
  Product = Palo Alto GlobalProtect
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  ParserVersion = v1.0.0
  Conditions = [ """,USERID,login,""" ]
  Fields = [
    """\s(-|({host}[\w\-.]+))\s+\d+,({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+).+?,USERID,login,""",
    """,USERID,login,.+?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),(({domain}[^\\\s,]+)\\+)?({user}[^\\\s,]+)""",
    """({app}active-directory)""",
  ]


}
```