#### Parser Content
```Java
{
Name = "trendmicro-officescan-kv-alert-trigger-success-officescanserver"
Vendor = "Trend Micro"
Product = "OfficeScan"
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
"""Spyware/Grayware:"""
"""SourceName =Trend Micro OfficeScan Server"""
]
Fields = [
"""ComputerName =({host}[^\s\n]+)"""
"""\sType=({alert_severity}[^\s\n]+)"""
"""User=(?:SYSTEM|NOT_TRANSLATED|({user}[\w\.\-]{1,40}\$?))"""
"""RecordNumber=({alert_id}\d+)"""
"""Spyware/Grayware:\s({alert_name}.+?)\s+Computer:"""
"""(Endpoint|Computer):\s+({src_host}[^\s\n]+)"""
]
DupFields = [
"alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```