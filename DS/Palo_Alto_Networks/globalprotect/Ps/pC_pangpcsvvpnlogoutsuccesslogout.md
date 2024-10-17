#### Parser Content
```Java
{
Name = pan-gp-csv-vpn-logout-success-logout
  ParserVersion = v1.0.0
  Vendor = Palo Alto Networks
  Product = GlobalProtect
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [
""",vpn-client,globalprotect,""",
""",USERID,logout,"""
  ]
  Fields = [
    """,USERID,logout,\S+,({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d),""",
    """,USERID,logout,.+?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^\\\s,]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^,]+)),""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
     """({serial_num}[^,]+),USERID,logout"""
    """,USERID,logout,([^,]*,){20}({device_name}[^,]+)"""
  ]
  

}
```