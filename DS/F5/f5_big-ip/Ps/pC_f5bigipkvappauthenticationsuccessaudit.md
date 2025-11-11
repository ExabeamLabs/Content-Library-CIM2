#### Parser Content
```Java
{
Name = f5-bigip-kv-app-authentication-success-audit
  ParserVersion = v1.0.0
  Vendor = F5
  Product = F5 BIG-IP
  TimeFormat = [ "yyyy-MM-dd HH:mm:ss" , "MMM dd HH:mm:ss" ]
  Conditions = [ """httpd(mod_auth_pam):""", """ user=""", """tty=""", """: AUDIT """ ]
  Fields = [
    """<(?:\d{1,3})>(?:\d{0,2}\s)?({time}\w{3}\s+\d{1,2}\s+\d{2}:\d{2}:\d{2})"""
    """({host}[\w.-]+)\s({severity}notice)""",
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s+({event_code}\d+):""",
    """user=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """level=({role}\S+)\s+($|\w+=)""",
    """host=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]


}
```