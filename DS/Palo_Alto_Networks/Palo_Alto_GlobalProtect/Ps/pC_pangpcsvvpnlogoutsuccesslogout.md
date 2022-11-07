#### Parser Content
```Java
{
Name = pan-gp-csv-vpn-logout-success-logout
  ParserVersion = v1.0.0
  Vendor = Palo Alto Networks
  Product = Palo Alto GlobalProtect
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [
""",vpn-client,globalprotect,""",
""",USERID,logout,"""
  ]
  Fields = [
    """,USERID,logout,\S+,({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d),""",
    """,USERID,logout,.+?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),(({domain}[^\\\s,]+)\\+)?({user}[^\\\s,]+)"""
  ]
  

}
```