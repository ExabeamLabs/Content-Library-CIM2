#### Parser Content
```Java
{
Name = cylance-cylance-xml-app-notification-8
  Vendor = Cylance
  Product = Cylance
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<Event xmlns=""", """<Provider Name ='CylanceSvc'""", """>8</EventID>""" ]
  Fields = [
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """<Computer>({host}.+?)<\/Computer>""",
    """>({event_code}\d+)<\/EventID>""",
    """<Provider Name ='({provider_name}[^']+)'""",
    """<Message>({event_name}.+?)<\/Message>""",
    """Connected  Device:\s*({src_host}[\w\-.]+)""",
    """IP:\s*({src_ip}[A-Fa-f:\d.]+)""",
    """MAC:\s*({src_mac}[^\s,;<]+)""",
  ]


}
```