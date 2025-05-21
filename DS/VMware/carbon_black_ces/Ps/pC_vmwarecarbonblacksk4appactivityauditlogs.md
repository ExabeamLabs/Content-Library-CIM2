#### Parser Content
```Java
{
Name = vmware-carbonblack-sk4-app-activity-auditlogs
  ParserVersion = "v1.0.0"
  Vendor = VMware
  Product = Carbon Black CES
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """destinationServiceName =CB Defense""", """"loginName":""",  """dproc=auditlogs""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"loginName":"(({email_address}[^"]+@[^"]+)|(({domain}[^"\\]+)\\{2})?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """eventId":"({event_code}[^"]+)""",
    """clientIp":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """description":"({additional_info}[^"]+?)\s*"""",
    """({app}CB Defense)"""
  ]


}
```