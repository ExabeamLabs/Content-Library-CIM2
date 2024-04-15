#### Parser Content
```Java
{
Name = "sophos-ep-kv-alert-trigger-success-728"
Vendor = "Sophos"
Product = "Sophos Endpoint Protection"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""", ThreatName =""""
""", ActionTakenName =""""
""", ThreatTypeName =""""
]
Fields = [
"""EventID="({alert_id}\d+)"""
"""FirstDetectedAt="({time}\d\d\d\d\-\d\d-\d\d \d\d:\d\d:\d\d)"""
"""ThreatTypeName ="({alert_type}[^"]+)"""
"""ThreatName ="({alert_name}[^"]+)"""
"""ActionTakenName ="({action}[^"]+)"""
"""FullFilePath="C:\\Users\\({user}[^\\]+)"""
"""UserName ="((NT AUTHORITY|({domain}[^\\\s"]+))\\+)?(SYSTEM|({user}[^\\\s"]+))"""
"""ComputerName ="({src_host}[\w\-.]+)"""
"""FullFilePath="({malware_url}[^"]+?({malware_file_name}[^"\\]+))""""
]
ParserVersion = "v1.0.0"


}
```