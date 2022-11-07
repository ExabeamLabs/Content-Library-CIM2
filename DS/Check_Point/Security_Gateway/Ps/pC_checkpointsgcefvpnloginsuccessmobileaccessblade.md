#### Parser Content
```Java
{
Name = checkpoint-sg-cef-vpn-login-success-mobileaccessblade
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """|Check Point|Mobile Access Blade|""", """|RAS Log In|""" ]

cef-checkpoint-vpn-events = {
  Vendor = Check Point
  Product = Security Gateway
  TimeFormat = "epoch"
  Fields = [
    """\Wrt=({time}\d+)""",
    """\Wdvc=({host}[A-Fa-f:\d.]+)""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """\WAction:\s*({action}[^;]+)""",
    """\Wshost=({src_host}[\w\-.]+)""",
    """\Wsrc=({src_ip}[A-Fa-f:\d.]+)""",
    """\Wsuser=({user}[^\s]+)""",
    """\WsourceGeoCountryCode=({src_country_code}\w+)"""
  ]
   DupFields = [ "action->event_name" 
}
```