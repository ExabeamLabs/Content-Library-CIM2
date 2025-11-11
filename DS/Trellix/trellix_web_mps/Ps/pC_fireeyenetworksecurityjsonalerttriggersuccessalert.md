#### Parser Content
```Java
{
Name = "fireeye-networksecurity-json-alert-trigger-success-alert"
Vendor = "Trellix"
Product = "Trellix Web MPS"
TimeFormat = ["yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ssZ"]
Conditions = [
  """"msg": """"
  """"product": "Web MPS""""
  """"alert": {"""
]
Fields = [
  """"appliance": "({host}[^"]+)"""",
  """"src":\s\{\s*(?:"\w+": "[^"]+",\s*)*"ip": "({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
  """"src":\s\{\s*(?:"\w+": "[^"]+",\s*)*"host": "({src_host}[^"]+)"""",
  """"explanation":\s\{\s*(?:"\w+": "[^"]+",\s*)*"({alert_type}[^"]+)": \{\s*[^\{]+\{\s*(?:"\w+": "[^"]+",\s*)*"name": "({alert_name}[^"]+)"""",
  """"severity": "({alert_severity}[^"]+)"""",
  """"occurred": "({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2})""",
  """"id": "({alert_id}[^"]+)",""",
  """"dst":\s*\{\s*"ip":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""""
  """"dst":\s*\{[^\}]+?"port":\s*"({dest_port}\d+)""""
  """"src":\s*\{[^\}]+?"port":\s*"({src_port}\d+)""""
  """"proxy":\s*"({proxy_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """"malware":\s*\{[^\}]+?"name":\s*"({alert_name}[^"]+)""""
  """"dst":\s*\{[^\}]+?"mac":\s*"({dest_mac}[^"]+)""""
  """"src":\s*\{[^\}]+?"mac":\s*"({src_mac}[^"]+)""""
  """"alert":\s\{[^\}]+?"alert-url":\s*"({event_url}[^"]+)""""
  """"occurred":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""""
]
ParserVersion = "v1.0.0"


}
```