#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-lock-success-4800"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [ """"EventID":4800""", """The workstation was locked""" ]
Fields = [
""""TimeGenerated\\?":\\?"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
""""EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
""""(Hostname|Computer)":"({dest_host}({host}[^"]+))"""
"""({event_name}The workstation was locked)"""
"""({event_code}4800)"""
"""Account Name:\s*(\\t|\\r|\\n)*({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\\t|\\r|\\n)*\s*Account Domain"""
"""Account Domain:\s*(\\t|\\r|\\n)*({domain}.+?)(\\t|\\r|\\n)*\s*Logon ID"""
"""Logon ID:\s*(\\t|\\r|\\n)*({login_id}.+?)(\\t|\\r|\\n)*\s*Session"""
]
ParserVersion = "v1.0.0"


}
```