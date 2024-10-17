#### Parser Content
```Java
{
Name = checkpoint-sg-cef-vpn-login-success-mobileaccessblade
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """|Check Point|Mobile Access Blade|""", """|RAS Log In|""" ]

cef-checkpoint-vpn-events = {
  Vendor = Check Point
  Product = Check Point Security Gateway
  TimeFormat = "epoch"
  Fields = [
    """\Wrt=({time}\d{13})""",
    """\Wdvc=({host}[A-Fa-f:\d.]+)""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """\WAction:\s*({action}[^;]+)""",
    """\Wshost=({src_host}[\w\-.]+)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wsuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """\WsourceGeoCountryCode=({src_country_code}\w+)"""
  ]
   DupFields = [ "action->event_name" 
}
```