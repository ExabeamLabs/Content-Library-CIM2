#### Parser Content
```Java
{
Name = "hp-arubacpm-kv-app-notification-success-catchallsystemevents"
Conditions = [ """SystemEvents""", """Component=""", """Category=""", """Timestamp=""" ]
ParserVersion = "v1.0.0"

aruba-clearpass-policy}{
Name = "hp-arubacpm-kv-app-notification-success-catchallsystemevents"
Conditions = [ """SystemEvents""", """Component=""", """Category=""", """Timestamp=""" ]
ParserVersion = "v1.0.0"
},
${HPEParsersTemplates.aruba-clearpass-policy}{
Name = "hp-arubacpm-kv-app-notification-success-catchallauditevents"
Conditions = [ """Audit logs""", """Category=""", """Timestamp=""" ]
ParserVersion = "v1.0.0"
},

{
Name = "microsoft-evsystem-str-endpoint-notification-success-mswineventlog"
Vendor = "Microsoft"
Product = "Event Viewer - System"
Conditions = [
""" - MSWinEventLog -"""
"""Snare_Enterprise_Agent_for_Windows"""
]
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "MMM dd HH:mm:ss yyyy"]
  Fields = [
    """\s({time}[a-zA-Z]{3} \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})"""
    """({time}\d{1,4}-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """[^\s]+\s+\-?\s*({event_code}\d+)\s+\w{3}\s\w{3}"""
    """({host}[\w\-\.]+)\s+None"""
    """\s({src_ip}((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({src_port}\d+))?\s+[^\s]+\s+\-?\s*MSWinEventLog"""
    """({log_name}MSWinEventLog)"""
  ]
ParserVersion = "v1.0.0"
}

{
  Name = tenable-tie-str-app-notification-success-tenablead
  ParserVersion = v1.0.0
  Vendor = Tenable
  Product = Tenable Identity Exposure
  TimeFormat = ["MMM  d HH:mm:ss", "MMM dd HH:mm:ss"]
  Conditions = [ """Tenable.ad[""", """ "3" """ ]
  Fields = [
    """({time}\w{3}\s+\d{1,2}\s\d\d:\d\d:\d\d)"""
    """\s\d\d:\d\d:\d\d\s({host}[\w.-]+)"""
    """({app}Tenable.ad)"""
    """Tenable\.ad\s*\[({process_id}\d+)\]"""
    """Tenable\.ad\s*\[\S+]:\s"({event_code}\d+)""""
    """Tenable\.ad\s*\[\S+\]:\s"[^"]*"\s"({alert_id}\d+)""""
    """Tenable\.ad\s*\[\S+\]:\s("[^"]*"\s){2}"({event_name}[^"]+)""""
    """Tenable\.ad\s*\[\S+\]:\s("[^"]*"\s){3}"({result}[^\s]+)""""
    """Tenable\.ad\s*\[\S+\]:\s("[^"]*"\s){4}"({domain}[^"]+)""""
    """"ComputerCn"="?({host}[\w\-.]+)"?"""
    """"OperatingSystem"="?({os}[^"]+)"?"""
    """"OperatingSystemVersion"="?({os_version}[^"]+)"?"""
  ]
  DupFields = [ "event_name->operation" 
}
```