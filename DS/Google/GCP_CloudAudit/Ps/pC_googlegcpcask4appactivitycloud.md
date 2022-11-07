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
     """"timestamp":({time}\d+)""",
     """"callerIp":"({src_ip}[a-fA-F\d.:]+)""",
     """"serviceName":"({app}[^"]+)""",
     """"methodName":"({operation}[^"]+)""",
     """"principalEmail":"(({email_address}[^@\s"]+?@({email_domain}[^\s@"]+?))|({user}[^\s"]+?))"""",
     """"callerSuppliedUserAgent":"({user_agent}[^"]+)""",
     """"resource"[^=]*?project_id":"({account}[^"]+)""",
     """"resource"[^=]*?"type":"({resource_type}[^"]+)""",
     """"resourceName":\s*"({resource}[^"]+)""",
     """"permission":"({permission}[^"]+)""",
     """"granted":({result}[^,":\}]+)"""
  ]
  DupFields = [ "resource->object" ]


}
```