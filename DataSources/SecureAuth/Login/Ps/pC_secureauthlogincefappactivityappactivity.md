#### Parser Content
```Java
{
Name = secureauth-login-cef-app-activity-appactivity
  Vendor = SecureAuth
  Product = Login
  TimeFormat = "epoch"
  Conditions = [
    """CEF:""",
    """|SecureAuth|"""
  ]
  Fields = [
    """\WdeviceCustomDate1=({time}\d+)""",
    """\Wdvc=({host}.+?)\s+(\w+=|$)""",
    """\Wsuser=({user}[^\s]+)\s+(\w+=|$)""",
    """\Wsrc=({dest_host}.+?)\s+(\w+=|$)""",
    """\WrequestClientApplication=({user_agent}.+?)\s+(\w+=|$)""",
    """\Wmsg=({event_name}.+?)\s+(\w+=|$)"""
  ]
  ParserVersion = "v1.0.0"


}
```