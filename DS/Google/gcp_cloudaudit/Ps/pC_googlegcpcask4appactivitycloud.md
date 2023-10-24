#### Parser Content
```Java
{
Name = google-gcpca-sk4-app-activity-cloud
  ParserVersion = "v1.0.0"
  Vendor = Google
  Product = GCP CloudAudit 
  TimeFormat = "epoch"
  Conditions = [ """destinationServiceName =Google Cloud Platform""", """"resource"""", """"project_id"""" ]
  Fields = [
     """"timestamp":({time}\d{13})""",
     """"callerIp":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """"serviceName":"({app}[^"]+)""",
     """"methodName":"({operation}[^"]+)""",
     """"principalEmail":"(({email_address}[^@\s"]+?@({email_domain}[^\s@"]+?))|({user}[\w\.\-]{1,40}\$?))"""",
     """"callerSuppliedUserAgent":"({user_agent}[^"]+)""",
     """"resource"[^=]*?project_id":"({account}[^"]+)""",
     """"resource"[^=]*?"type":"({resource_type}[^"]+)""",
     """"resourceName":\s*"({resource}[^"]+)""",
     """"permission":"({permission}[^"]+)""",
     """"granted":({result}[^,":\}]+)""",
     """requestClientApplication=\s*({app}[^=]+?)\s+\w+=""",
     """suser=\s*(anonymous|({email_address}[^@\s]+?@({email_domain}[^\s@\.]+?\.[^\s]+))|({user}[\w\.\-]{1,40}\$?))\s+\w+=""",
     """"region":"({region}[^"]+?)"""",
     """"severity":"({alert_severity}[^"]+?)"""" 
  ]
  DupFields = [ "resource->object" ]


}
```