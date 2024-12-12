#### Parser Content
```Java
{
Name = tenable-tie-str-alert-trigger-success-tenablead
  ParserVersion = v1.0.0
  Vendor = Tenable
  Product = Tenable Identity Exposure
  TimeFormat = ["MMM  d HH:mm:ss", "MMM dd HH:mm:ss"]
  Conditions = [ """Tenable.ad[""", """ "0" """, """=""" ]
  Fields = [
    """({time}\w{3}\s+\d{1,2}\s\d\d:\d\d:\d\d)"""
    """\s\d\d:\d\d:\d\d\s({host}[\w.-]+)"""
    """Tenable\.ad\s*\[({process_id}\d+)\]"""
    """Tenable\.ad\s*\[\S+]:\s"({event_code}\d+)"""
    """Tenable\.ad\s*\[\S+\]:\s"[^"]*"\s"({alert_id}\d+)"""
    """Tenable\.ad\s*\[\S+\]:\s("[^"]*"\s){2}"({alert_type}[^"]+)"""
    """Tenable\.ad\s*\[\S+\]:\s("[^"]*"\s){3}"({domain}[^"]+)""""
    """Tenable\.ad\s*\[\S+\]:\s("[^"]*"\s){4}"({alert_name}[^"]+)"""
    """Tenable\.ad\s*\[\S+\]:\s("[^"]*"\s){5}"({alert_severity}[^"]+)"""
    """Tenable\.ad\s*\[\S+\]:\s("[^"]*"\s){6}"({object_dn}[^"]+)"""
    """Tenable\.ad\s*\[\S+\]:\s("[^"]*"\s){9}"({alert_subject}[^"]+)"""
    """"AccountCn"="({account_name}[^"]+)"""
    """"GroupCn"="({group_name}[^"]+)"""
    """"SID"="({user_sid}[^"]+)"""
    """"Cn"="(({full_name}[^"\s]+\s+[^"\s]+)|({user}[^"\s]+))"""
  ]
  DupFields = [ alert_subject->result_reason ]


}
```