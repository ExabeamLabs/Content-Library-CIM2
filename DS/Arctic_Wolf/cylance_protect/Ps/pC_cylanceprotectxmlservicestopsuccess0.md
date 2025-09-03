#### Parser Content
```Java
{
Name = cylance-protect-xml-service-stop-success-0
  ParserVersion = v1.0.0
  Vendor = Cylance
  Product = Cylance PROTECT
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<Event xmlns=""", """<Provider Name ='CylanceSvc'""", """>0</EventID>""" ]
  Fields = [
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """<Computer>({host}.+?)<\/Computer>""",
    """>({event_code}\d+)<\/EventID>""",
    """<Provider Name ='({provider_name}[^']+)'""",
    """<Message>({event_name}.+?)<\/Message>""",
  ]


}
```