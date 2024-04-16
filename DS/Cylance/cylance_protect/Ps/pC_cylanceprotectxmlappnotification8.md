#### Parser Content
```Java
{
Name = cylance-protect-xml-app-notification-8
  Vendor = Cylance
  Product = Cylance PROTECT
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
    """IP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """MAC:\s*({src_mac}[^\s,;<]+)""",
  ]


}
```