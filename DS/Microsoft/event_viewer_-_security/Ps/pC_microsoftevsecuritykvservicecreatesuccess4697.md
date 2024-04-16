#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-service-create-success-4697"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["MM/dd/yyyy hh:mm:ss a", "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "MMM dd HH:mm:ss yyyy", "epoch"]
Conditions = [
"""4697"""
"""A service was installed in the system"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\s+(Mon|Tue|Wed|Thu|Fri|Sat|Sun)\s+({time}\w+ \d+ \d+:\d+:\d+ \d+)\s+"""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,9})?Z)"""
"""({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (am|AM|pm|PM))"""
"""({event_code}4697)"""
"""({event_name}A service was installed in the system)"""
"""\sComputerName =(|({host}[\w\-.]+?))(\s+\w+=|\s*$)"""
"""\sKeywords=(|({result}.+?))(\s+\w+=|\s*$)"""
"""Security ID:\s*(|({user_sid}.+?))(\\[nrt]\s+|\s*)Account Name:\s*(|({user}[\w\.\-]{1,40}\$?))(\\[nrt]\s+|\s*)Account Domain:\s*(|({domain}.+?))(\\[nrt]\s+|\s*)Logon ID:\s*(|({login_id}.+?))((\\[nrt])+\s*|\s*)Service Information:"""
"""\sdestinationServiceName =({service_name}[^=]+?)\s+\w+="""
"""\sService Name:\s*(|({service_name}[^:]+?)(_[0-9a-f]+)?)\s"""
"""\sService Type:\s*(|({service_type}.+?))(\\[nrt]\s+|\s)"""
"""filePath=\s*\"*(?:|-|({process_path}({process_dir}(?:[^\";]+)?[\\\/])?({process_name}.*?)))\\?\"""",
"""\sService File Name:\s*\"*(|({process_path}({process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({process_name}[^\\\/\"]+?)))\"*\s"""
"""\sService Start Type:\s*(|({service_start_type}.+?))(\\[nrt]\s+|\s)"""
"""Service Account:\s*(({account_domain}[^\\"\s]+)\\)?({account_name}[^"\s]+)"""
"""Computer(\w+)?[\"\s]*(:|=)\s*\"?({host}[\w\-.]+?)(\"|\s)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```