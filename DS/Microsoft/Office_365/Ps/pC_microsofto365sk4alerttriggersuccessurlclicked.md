#### Parser Content
```Java
{
Name = microsoft-o365-sk4-alert-trigger-success-urlclicked
Vendor = "Microsoft"
Product = "Office 365"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""""Operation":"TIUrlClickData""""
"""destinationServiceName =Office 365"""
]
Fields = [
""""CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""""
""""Id":"({alert_id}[^"]+)""""
""""EventDeepLink":"\s*({additional_info}[^"]+)""""
""""Workload":"({alert_type}[^"]+)"""
""""Operation":"({alert_name}[^"]+)"""
""""UserId":"({email_address}[^@"\s]+?@[^"\s]+?)""""
""""UserIp":"({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))""""
""""Url":"({malware_url}[^"]+?)""""
]
ParserVersion = "v1.0.0"


}
```