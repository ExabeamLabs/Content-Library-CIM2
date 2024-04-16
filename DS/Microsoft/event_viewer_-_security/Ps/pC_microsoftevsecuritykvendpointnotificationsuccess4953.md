#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-notification-success-4953
Vendor = Microsoft
Product = Event Viewer - Security
ParserVersion = "v1.0.0"
TimeFormat = "MM/dd/yyyy hh:mm:ss a"
Conditions = [ """EventCode=4953""", """ComputerName =""", """RecordNumber=""","""Microsoft Windows security auditing""" ]
Fields = 
[
    """({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(?i)(AM|PM))"""
    """\WLogName =({log_name}[^\s]+)"""
    """\WSourceName =({service_name}.+?)(\s+\w+=|\s*$)"""
    """\WEventCode=({event_code}\d+)"""
    """\WComputerName =({host}[\w\-.]+)"""
    """TaskCategory=({task}[^=]+?)\s*\w+="""
    """RecordNumber=({event_id}\d+)"""
    """Keywords=({result}.+?);?\s*Message="""
    """Message=({event_name}[^\.]+)"""
    """ID:\s*({rule_id}[^\s]+)\s"""
]


}
```