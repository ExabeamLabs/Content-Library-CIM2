#### Parser Content
```Java
{
Name = code42-incydr-sk4-app-activity-success-appclient
  Vendor = Code42
  Product = Code42 Incydr
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions= [ """"actorType": "API_CLIENT"""", """"actorName"""", """"success":""", """Code42""" ]
  Fields = [
    """timestamp":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""",
    """destinationServiceName =({app}Custom Application)""",
    """"actorName":\s*"({user}[^"\s]+)""",
    """"audit_log:+({operation}[^"]+)""",
    """"actorIpAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"actorAgent":\s*"({user_agent}[^"]+)""""
  ]


}
```