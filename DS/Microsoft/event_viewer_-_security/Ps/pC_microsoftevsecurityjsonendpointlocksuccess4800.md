#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-lock-success-4800"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [ """"EventID":4800""", """The workstation was locked""" ]
Fields = [
""""EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
""""Hostname":"({host}[^"]+)"""
"""({event_name}The workstation was locked)"""
"""({event_code}4800)"""
"""Account Name:\s*((\\)[rnt])*({user}.+?)((\\)[rnt])*\s*Account Domain"""
"""Account Domain:\s*((\\)[rnt])*({domain}.+?)((\\)[rnt])*\s*Logon ID"""
"""Logon ID:\s*((\\)[rnt])*({login_id}.+?)((\\)[rnt])*\s*Session"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```