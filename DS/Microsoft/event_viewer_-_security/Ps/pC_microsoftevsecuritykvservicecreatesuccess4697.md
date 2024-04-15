#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-service-create-success-4697"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
"""4697"""
"""A service was installed in the system"""
]
Fields = [
"""({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (am|AM|pm|PM))"""
"""({event_code}4697)"""
"""({event_name}A service was installed in the system)"""
"""\sComputerName =(|({host}.+?))(\s+\w+=|\s*$)"""
"""\sKeywords=(|({result}.+?))(\s+\w+=|\s*$)"""
"""Security ID:\s*(|({user_sid}.+?))(\\[nrt]\s+|\s*)Account Name:\s*(|({user}.+?))(\\[nrt]\s+|\s*)Account Domain:\s*(|({domain}.+?))(\\[nrt]\s+|\s*)Logon ID:\s*(|({login_id}.+?))((\\[nrt])+\s*|\s*)Service Information:"""
"""\sService Name:\s*(|({service_name}.+?))(\\[nrt]\s+|\s)"""
"""\sService Type:\s*(|({service_type}.+?))(\\[nrt]\s+|\s)"""
"""\sService File Name:\s*\"*(|({process_path}({process_dir}.*?[\\\/]+)?({process_name}[^\\\/\"]+?)))\"*\s"""
"""\sService Start Type:\s*(|({service_start_type}.+?))(\\[nrt]\s+|\s)"""
"""Service Account:\s*(({account_domain}[^\\]+)\\)?({account_name}[^=]+?)\s*($|\w+=)"""
"""Computer(\w+)?[\"\s]*(:|=)\s*\"?({host}.+?)(\"|\s)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```