#### Parser Content
```Java
{
Name = "microsoft-evsystem-str-service-create-success-7045"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
"""7045"""
"""A service was installed in the system."""
]
Fields = [
"""EventTime\":\"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\""""
"""({event_name}A service was installed in the system)"""
"""ComputerName =({host}[\w-.]+)\s"""
"""\WComputer=({host}[\w\-.]+)\s"""
"""({host}\S+)\sEvntSLog"""
"""({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(?i)(AM|PM))"""
"""\]\s+\w{3}\s({time}\w{3}\s\d+\s\d\d:\d\d:\d\d\s\d\d\d\d)"""
"""TimeGenerated=({time}\d+)"""
"""({event_code}7045)"""
"""AccountName\":\"((?i)SYSTEM|NOT_TRANSLATED|({user}[^\"]+))\""""
"""User=((?i)NOT_TRANSLATED|({user}[^\s]+))"""
"""\w{3}\s\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d:\s({domain}[^\\]+)\\(\\)?((?i)NOT_TRANSLATED|({user}[^\/]+))"""
"""Service Name:\s+({service_name}[^=:]+?)\s*Service File Name:"""
"""Service File Name:\s+(|-|({process_path}({process_dir}(?:[^\"]+)?[\\\/])?({process_name}[^\\\/\s]+)))\s+Service Type:"""
"""Service File Name:\s*((?:[^\";]+)?[\\\/;])?({process_name}[^\\\/\";]+?\.[^\\\/\.;\"]+?)\s.*?\s*Service Type:"""
"""Service Type:\s+({service_type}[^=:]+?)\s*Service Start Type:"""
"""Service Account:\s*(|(({account_domain}[^\\]+)\\)?({account_name}[^\"]+?))\s*(\"|$)"""
"""Service File Name:\s*({process_command_line}[^=]+?)\s*Service Type:"""
"""ComputerName(:|=)\s*({host}[\w.-]+)"""
"""TimeStamp:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
"""User:\s*((?i)NOT_TRANSLATED|({user}[^:]+?))\s*\w+:"""
]
DupFields = [
"host->dest_host"
"process_command_line->service_command_line"
]
ParserVersion = "v1.0.0"


}
```