#### Parser Content
```Java
{
Name = "trendmicro-officescan-kv-alert-trigger-success-trendmicro"
Vendor = "Trend Micro"
Product = "OfficeScan"
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
"""Virus/Malware:"""
"""SourceName =Trend Micro OfficeScan Server"""
]
Fields = [
"""ComputerName =({host}[^\s\n]+)"""
"""\sType=({alert_severity}[^\s\n]+)"""
"""User=(?:SYSTEM|NOT_TRANSLATED|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""RecordNumber=({alert_id}\d+)"""
"""Virus/Malware:\s({alert_name}.+?)\s+(Endpoint|Computer):"""
"""(Endpoint|Computer):\s+({src_host}[^\s\n]+)"""
"""File:\s+({malware_url}.+?)\s+Date"""
]
DupFields = [
"alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```