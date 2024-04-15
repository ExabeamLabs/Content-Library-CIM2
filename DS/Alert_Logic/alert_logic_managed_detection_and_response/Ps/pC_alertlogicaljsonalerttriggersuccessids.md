#### Parser Content
```Java
{
Name = "alertlogic-al-json-alert-trigger-success-ids"
Vendor = "Alert Logic"
Product = "Alert Logic Managed Detection and Response"
TimeFormat = "epoch_sec"
Conditions = [
""""source_keyword":"""
"""IDS"""
""""account_deployments":"""
""""associatedEventCount":"""
]
Fields = [
""""generator":\s*\{[^\}]*"time":\s*({time}\d{10})"""
""""generator":\s*\{[^\}]*"hostName":\s*"({host}[\w\-.]+)"""
""""victims":\s*\["({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
""""attacker":\s*\[\{[^\}]*"ip":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""incidentId":\s*"({alert_id}[^"]+)"""
""""summary":\s*"({alert_name}[^"]+?)\s+from [A-Fa-f:\d.]+"""
""""threatRating":\s*"({alert_severity}[^"]+)"""
""""incident":\s*\{.*?"type":\s*"({alert_type}[^"]+)"""
""""facts_url":\s*"({additional_info}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```