#### Parser Content
```Java
{
Name = "microsoft-windows-str-log-clear-success-104"
Vendor = "Microsoft"
Product = "Windows"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
""" 104 """
"""Microsoft-Windows-Eventlog"""
"""log file was cleared."""
]
Fields = [
"""({host}\S+)\s+MSWinEventLog\s+\S+\s+\S+\s+\S+\s+\S+\s+({time}\w+ \d+ \d\d:\d\d:\d\d \d+)\s+({event_code}104)\s+Microsoft-Windows-Eventlog\s+(({domain}[^\\]+?)[\\\/]+)?({user}[^\s]+)"""
"""(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w\-\.]+))\s+MSWinEventLog\s+"""
"""({event_name}The.*?log file was cleared.)"""
]
DupFields = [ "host->dest_host" ]
ParserVersion = "v1.0.0"


}
```