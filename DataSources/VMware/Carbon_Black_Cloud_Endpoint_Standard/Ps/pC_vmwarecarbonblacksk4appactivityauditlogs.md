#### Parser Content
```Java
{
Name = vmware-carbonblack-sk4-app-activity-auditlogs
  ParserVersion = "v1.0.0"
  Vendor = VMware
  Product = Carbon Black Cloud Endpoint Standard
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """destinationServiceName =CB Defense""", """"loginName":""",  """dproc=auditlogs""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"loginName":"(({email_address}[^"]+@[^"]+)|(({domain}[^"\\]+)\\{2})?({user}[^"]+))"""",
    """eventId":"({event_code}[^"]+)""",
    """clientIp":"({src_ip}[a-fA-F\d.:]+)""",
    """description":"({additional_info}[^"]+?)\s*"""",
    """({app}CB Defense)"""
  ]


}
```