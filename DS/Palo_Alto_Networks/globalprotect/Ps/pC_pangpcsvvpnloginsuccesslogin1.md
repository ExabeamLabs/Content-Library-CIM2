#### Parser Content
```Java
{
Name = pan-gp-csv-vpn-login-success-login-1
  ParserVersion = v1.0.0
  Vendor = Palo Alto Networks
  Product = GlobalProtect
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [
""",vpn-client,globalprotect,""",
""",USERID,login,"""
  ]
  Fields = [
    """,USERID,login,\S+,({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d),""",
    """,USERID,login,.+?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),(({domain}[^\\\s,]+)\\+)?({user}[^\\\s,]+)"""
  ]


}
```