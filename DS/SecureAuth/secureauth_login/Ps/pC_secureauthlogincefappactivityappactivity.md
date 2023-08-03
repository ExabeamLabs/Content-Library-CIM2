#### Parser Content
```Java
{
Name = secureauth-login-cef-app-activity-appactivity
  Vendor = SecureAuth
  Product = SecureAuth Login
  TimeFormat = "epoch"
  Conditions = [
    """CEF:""",
    """|SecureAuth|"""
  ]
  Fields = [
    """\WdeviceCustomDate1=({time}\d{13})""",
    """\Wdvc=({host}.+?)\s+(\w+=|$)""",
    """\Wsuser=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))\s+(\w+=|$)""",
    """\Wsrc=(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}[\w\-.]+?))\s+(\w+=|$)""",
    """\WrequestClientApplication=({user_agent}.+?)\s+(\w+=|$)""",
    """\Wmsg=({event_name}.+?)\s+(\w+=|$)"""
  ]
  ParserVersion = "v1.0.0"


}
```