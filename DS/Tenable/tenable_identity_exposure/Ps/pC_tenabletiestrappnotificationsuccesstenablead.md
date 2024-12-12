#### Parser Content
```Java
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
  ]
  DupFields = [ "event_name->operation" ]


}
```