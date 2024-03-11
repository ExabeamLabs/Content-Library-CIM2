#### Parser Content
```Java
{
Name = microsoft-o365-json-app-activity-success-labelupdated
  Vendor = Microsoft
  Product = Microsoft 365
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions= [ """"Application": """, """"DeviceName": """, """"Operation": "SensitivityLabelUpdated"""", """"SensitivityLabelEventData": """]
  Fields = [
    """"CreationTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""", 
    """"Application":\s*"({app}[^"]+)"""",
    """"ClientIP":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"UserId":\s*"({email_address}[^@]+@({email_domain}[^"]+))"""",
    """"DeviceName":\s*"({src_host}[^"]+)""",
    """"Operation":\s*"({operation}[^"]+)"""",
    """"Platform":\s*"({os}[^"]+)"""",
    """"ObjectId":"({object_id}[^"]+)"""",
    """"LabelEventType":\s*({event_code}\d+)"""",
    """"SensitivityLabelEventData":\s*\{({additional_info}[^\}]+)\}"""
  ]
  ParserVersion = "v1.0.0"


}
```