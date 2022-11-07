#### Parser Content
```Java
{
Name = lastpass-l-sk4-app-activity-success-report
Vendor = LastPass
Product = LastPass
TimeFormat = "yyyy-MM-dd HH:mm:ss"
ParserVersion = "v1.0.0"
Conditions = [ """Action":""","""dproc=EventReporting""","""destinationServiceName =LastPass"""]
Fields = [
""""Time":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
""""IP_Address":"({src_ip}[a-fA-F\d:.]+)"""",
"""destinationServiceName =({app}[^=]+?)\s\w+=""",
""""+Action"+:"+({event_name}[^"]+)"+""",
""""Username"+:"+({email_address}[^@"]+@[^\."]+\.[^"]+)""",
""""Username"+:"+API:\s*({user}[^"]+)""",
""""+Action"+:"+({action}[^"]+)"+""",
""""+Data"+:"+({additional_info}[^"\}]+)""",
"""fname=({file_name}[^=]+?)\s+[\w]+=""",
"""filePermission=({access}[^=]+?)\s+[\w]+=""",
"""duser=({dest_user}[^=]+?)\s+[\w]+=""",
"""Resource:\s+({file_type}[^:]+)\s+::"""
]
DupFields = [ "event_name->operation" ]


}
```