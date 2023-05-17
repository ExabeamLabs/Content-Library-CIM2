#### Parser Content
```Java
{
Name = amazon-awsguardduty-sk4-alert-trigger-success-inspector
   ParserVersion = v1.0.0
   Vendor = Amazon
   Product = AWS GuardDuty
   TimeFormat = "epoch"
   Conditions = [ """CEF:""", """"service":"Inspector"""", """destinationServiceName =AWS""" ]
   Fields = [
     """"createdAt":({time}\d{13}),""",
     """"hostname":"(localhost|({host}[\w.-]+?))"""",
     """"privateIpAddresses":[^\}]+?,"privateIpAddress":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
     """"service":"({service_name}[^"]+?)"""",
     """"severity":"({alert_severity}[^"]+?)"""",
     """"title":"({additional_info}[^"]+?)\s*",""""
    ]


}
```