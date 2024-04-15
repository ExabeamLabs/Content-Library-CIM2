#### Parser Content
```Java
{
Name = "symantec-esc-json-alert-trigger-success-squrlrecipient"
Vendor = "Symantec"
Product = "Symantec Email Security"
TimeFormat = "epoch"
Conditions = [ """"eventType": """", """"squrlClickerIp": """", """"squrlRecipient": """", """"severity": """", """"url": """" ]
Fields = [
""""timestamp_ms":\s*({time}\d{13})"""
""""squrlRecipient":\s*\"({email_address}[^\"\s@;,]+@[^\"\s@;,]+)"""
""""url":\s*\"({malware_url}[^\"]+)\""""
""""severity":\s*\"({alert_severity}[^\"]+)\""""
""""action":\s*\"({action}[^\"]+)\""""
""""squrlClickerIp":\s*\"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\""""
""""eventType":\s*\"({alert_name}[^\"]+)\""""
]
DupFields = [
"alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```