#### Parser Content
```Java
{
Name = vmware-carbonblack-sk4-app-activity-cbdefense
  ParserVersion = "v1.0.0"
  Vendor = VMware
  Product = Carbon Black Cloud Endpoint Standard
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """destinationServiceName =CB Defense""", """"loginName":""", """policy""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"loginName":"(({user}[^"@]+)|({email_address}[^"]+@[^"]+))"""",
    """eventId":"({event_code}[^"]+)""",
    """clientIp":"({src_ip}[a-fA-F\d.:]+)""",
    """description":"({additional_info}[^"]+?)\s*"""",
    """({app}CB Defense)""",
  ]


}
```