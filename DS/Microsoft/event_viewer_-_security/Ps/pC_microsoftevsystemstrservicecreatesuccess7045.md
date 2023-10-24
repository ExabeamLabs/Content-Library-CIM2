#### Parser Content
```Java
{
Name = "microsoft-evsystem-str-service-create-success-7045"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "MM/dd/yyyy HH:mm:ss a", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd HH:mm:ss", "MM/dd/yyyy hh:mm:ss a"]
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
"""AccountName\":\"((?i)SYSTEM|NOT_TRANSLATED|({user}[\w\.\-]{1,40}\$?))\""""
"""User=((?i)NOT_TRANSLATED|({user}[\w\.\-]{1,40}\$?))"""
"""\w{3}\s\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d:\s({domain}[^\\]+)\\(\\)?((?i)NOT_TRANSLATED|({user}[\w\.\-]{1,40}\$?))"""
"""Service Name:\s*({service_name}[^=:\\]+?)\s*(\\r|\\t|\\n)*Service File Name:"""
"""Service File Name:\s+(|-|({process_path}({process_dir}[^\"=]+?[\\\/])?({process_name}[^\\\/\s]+)))\s*(\\t|\\n|\\r)*Service Type"""
"""Service File Name:\s*((?:[^\";]+)?[\\\/;])?({process_name}[^\\\/\";]+?\.[^\\\/\.;\"]+?)\s.*?\s*Service Type:"""
"""Service Type:\s+({service_type}[^\\:=]+?)\s*(\\r|\\t|\\n)*Service Start Type:"""
"""Service Account:\s*(|(({account_domain}[^\s"]+)\\)?({account_name}.+?))\s*(\"|$|<)"""
"""Service File Name:\s*({process_command_line}[^=]+?)\s*(\\t|\\r|\\n)*Service Type:"""
"""ComputerName(:|=)\s*({host}[\w.-]+)"""
"""TimeStamp:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
"""User:\s*((?i)NOT_TRANSLATED|({user}[\w\.\-]{1,40}\$?))\s*\w+:"""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (AM|PM|am|pm))"""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,9})?Z)"""
]
DupFields = [
"host->dest_host"
"process_command_line->service_command_line"
]
ParserVersion = "v1.0.0"


}
```