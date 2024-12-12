#### Parser Content
```Java
{
Name = netskope-sc-json-app-login-success-loginsuccess
  Vendor = Netskope
  Product = Netskope Security Cloud
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"audit_log_event":""" , """"Login Successful"""", """"type":""", """"event-name":""", """"login-success"""", """"src-application-name":""", """"Netskope"""" ]
  Fields = [
    """"time":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""",
    """"user":\s*"(unknown|({email_address}[^@"]+@[^\."]+\.[^"]+))""",
    """"audit_log_event":\s*"({event_name}[^"]+)""",
    """"({operation}login-success)"""",
    """"src-ip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"({app}Netskope)""""
  ]


}
```