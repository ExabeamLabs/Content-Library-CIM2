#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-user-privilege-assign-success-4672-4
  Vendor = Microsoft
  Product = Event Viewer - Security 
  ParserVersion = "v1.0.0"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd HH:mm:ss"]
  Conditions = [ """"EventID":4672""", """"Message":"Special privileges assigned to new logon""", """"Microsoft-Windows-Security-Auditing"""" ]
  Fields = [
    """({event_name}Special privileges assigned to new logon)""",
	  """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """({event_code}4672)""",
    """"Computer(Name)?":"({host}[^"]+)"""",
    """Account Name:\s*(\\t|\\r|\\n)*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*(\\t|\\r|\\n)*Account Domain""",
    """Account Domain:\s*(\\t|\\r|\\n)*({domain}[^:]+?)\s*(\\t|\\r|\\n)*Logon ID:""",
    """Logon ID:\s*(\\t|\\r|\\n)*({login_id}[^:]+?)\s*(\\t|\\r|\\n)*Privileges:""",
    """Privileges:\s*(\\t|\\r|\\n)*({privileges}.+?)\s*(\\t|\\r|\\n)*(,\d+|\s*$|",)"""
  ]


}
```