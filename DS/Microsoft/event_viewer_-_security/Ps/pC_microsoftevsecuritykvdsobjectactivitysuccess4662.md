#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-ds-object-activity-success-4662"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "MM/dd/yyyy hh:mm:ss a", "MMM dd HH:mm:ss yyyy"]
Conditions = [
"""An operation was performed on an object"""
"""4662 """
]
Fields = [
"""({event_name}An operation was performed on an object)"""
"""({event_code}4662)"""
"""({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(?i)(AM|PM))"""
"""({time}\w+ \d\d \d\d:\d\d:\d\d \d\d\d\d)\s+"""
"""<TimeCreated SystemTime\\*=('|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d+Z'/>"""
""""EventTime"*:"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
"""\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+Microsoft-Windows-Security-Auditing"""
"""Computer(Name)?\s*\\*"?(=|:|>)\s*"*({host}[\w\.-]+)(\s|,|"|</Computer>|$)"""
"""({host}[^\s=]+)\sMSWinEventLog"""
"""Security ID:(\\t|\\r|\\n)*\s*(|({user_sid}[^:]+?))(\\t|\\r|\\n)*\s*Account Name:"""
"""Account Name:(\\r|\\n|\\t|\s)*((-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))(\\r|\\n|\\t|\s)*Account Domain:"""
"""Account Domain:(\\t|\\r|\\n)*\s*(|({domain}[^:]+?))(\\t|\\r|\\n)*\s*Logon ID:"""
"""Object Server:(\\t|\\r|\\n)*\s*(|({object_server}[^:]+?))(\\t|\\r|\\n)*\s*Object Type:"""
"""Object Type:(\\t|\\r|\\n)*\s*(|({object_type}[^:]+?))(\\t|\\r|\\n)*\s*Object Name:"""
"""Object Name:(\\t|\\r|\\n)*\s*(|({object_name}[^:]+?))(\\t|\\r|\\n)*\s*Handle ID:"""
"""Logon ID:(\\t|\\r|\\n)*\s*({login_id}[^\\\s]+)(\\t|\\r|\\n)*\s*"""
"""Operation Type:\s*({operation}[^:]+?)\s+Accesses:"""
"""Properties:(\\t|\\r|\\n)*\s*(-|({properties}[^:]+?))(\\t|\\r|\\n)*\s*Additional Information:"""
"""Access Mask:(\\t|\\r|\\n)*\s*({access_mask}[^\\\s]+)(\\t|\\r|\\n)*"""
""""ComputerName":"({host}[\w\-.]+)"""
""""EventType":"({operation_type}[^"]+?)""""
"""Accesses:\s*({access}[^:]+?)\s*Access Mask:"""
]
DupFields = [ "object_name->object" ]
ParserVersion = "v1.0.0"


}
```