#### Parser Content
```Java
{
Name = "sophos-ep-kv-app-activity-fail-blocked"
Vendor = "Sophos"
Product = "Sophos Endpoint Protection"
TimeFormat = [ "yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ssZ" ]
Conditions = [
"""Action=Blocked;"""
"""EventType=Application control;"""
"""ReportingName ="""
"""ComputerIPAddress="""
]
Fields = [
"""EventID=({event_code}[\d]+);"""
"""EventTime=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d\d:\d\d)""",
"""EventTime=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
"""EventType=({operation}[^;]+);"""
"""Name =({app}[^;]+);"""
"""UserName =([^\\]+\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?);"""
"""Action=({result}[^;]+);"""
"""({additional_info}SubType=[^;]+)"""
"""ComputerName =({src_host}[^;]+);"""
"""ComputerIPAddress=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""ComputerDomain=({domain}[^;]+)"""
]
ParserVersion = "v1.0.0"


}
```