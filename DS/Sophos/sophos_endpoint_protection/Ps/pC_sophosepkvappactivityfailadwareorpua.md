#### Parser Content
```Java
{
Name = "sophos-ep-kv-app-activity-fail-adwareorpua"
Vendor = "Sophos"
Product = "Sophos Endpoint Protection"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""Action=Blocked;"""
"""EventType=Adware or PUA;"""
"""ReportingName ="""
"""ComputerIPAddress="""
]
Fields = [
"""EventID=({event_code}[\d]+);"""
"""EventTime=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
"""EventType=({operation}[^;]+);"""
"""Name =({app}[^;]+);"""
"""UserName =([^\\]+\\+)?({user}[^;]+);"""
"""Action=({result}[^;]+);"""
"""({additional_info}SubType=[^;]+)"""
"""ComputerName =({src_host}[^;]+);"""
"""ComputerIPAddress=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""ComputerDomain=({domain}[^;]+)"""
"""SubType=({failure_reason}[^;]+)"""
]
ParserVersion = "v1.0.0"


}
```