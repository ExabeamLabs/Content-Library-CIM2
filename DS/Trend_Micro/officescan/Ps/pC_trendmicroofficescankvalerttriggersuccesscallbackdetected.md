#### Parser Content
```Java
{
Name = "trendmicro-officescan-kv-alert-trigger-success-callbackdetected"
Vendor = "Trend Micro"
Product = "OfficeScan"
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
"""C&C callback detected"""
"""SourceName =Trend Micro OfficeScan Server"""
]
Fields = [
"""ComputerName =({host}[^\s\n]+)"""
"""\sType=({alert_severity}[^\s\n]+)"""
"""User=(?:SYSTEM|NOT_TRANSLATED|({user}[^\s\n]+))"""
"""RecordNumber=({alert_id}\d+)"""
"""C\&C\s+({alert_name}.+?)\s+Compromised Host:"""
"""(Endpoint|Computer|Compromised Host):\s+({src_host}[^\s\n]+)"""
"""IP Address:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
DupFields = [
"alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```