#### Parser Content
```Java
{
Name = "microsoft-o365-cef-alert-trigger-success-anonymousipriskevent"
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""destinationServiceName =Office 365"""
""""riskEventType":"AnonymousIpRiskEvent""""
]
Fields = [
""""riskEventDateTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""requestClientApplication=({process_path}.+?)\s*(\w+=|$)"""
""""userPrincipalName":"({email_address}[^@\"\s]+?@[^\"\s]+?)\""""
""""id":"({alert_id}[^\"]+?)\""""
""""riskLevel":"({alert_severity}[^\"]+?)\""""
""""ipAddress\":"({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))\""""
""""riskEventType":\"({alert_name}[^\"]+?)\""""
"""({alert_type}anomalous-signin)"""
""""location":\{\"({additional_info}.*?)\}+"""
]
DupFields = [
"process_path->vendor_value"
"alert_type->alert_name"
]
ParserVersion = "v1.0.0"


}
```