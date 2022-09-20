#### Parser Content
```Java
{
Name = vmware-carbonblack-sk4-endpoint-login-success-cbdefense
  Vendor = VMware
  Product = Carbon Black Cloud Endpoint Standard
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """destinationServiceName =CB Defense""", """"loginName":""", """Logged in successfully""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"loginName":"(({user}[^"@]+)|({email_address}[^"]+@[^"]+))"""",
    """clientIp":"({dest_ip}[a-fA-F\d.:]+)""",
    """description":"({event_name}[^"]+)""",
    """({app}CB Defense)"""
  ]
  ParserVersion = "v1.0.0"


}
```