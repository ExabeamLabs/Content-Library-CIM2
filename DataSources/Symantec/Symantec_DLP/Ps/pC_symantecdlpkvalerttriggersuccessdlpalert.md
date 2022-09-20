#### Parser Content
```Java
{
Name = symantec-dlp-kv-alert-trigger-success-dlpalert
    Vendor = Symantec
    Product = Symantec DLP
    TimeFormat = "dd MMM yyyy HH:mm:ss.a"
    Conditions = [ """Policy Violated: """, """Endpoint Machine: """, """DLP ALERT""", """Application Name: """, """Incident ID: """ ]
    Fields = [
      """\d\d:\d\d:\d\d\s+({host}[^\s]+)"""
      """Reported On:\s+({time}\d{0,2} \w+ \d{1,4} \d{0,2}:\d{0,2}:\d{0,2} (am|pm|PM|AM))"""
      """\sPolicy Violated:\s+({alert_name}[^:]+?)\s*Reported On:""",
      """({additional_info}DLP ALERT|DLP ALERT[^:]+?)\s+Application Name:""",
      """\sApplication Name:\s+({app}[^:]+?)\s*Endpoint Machine:"""
      """\WEndpoint Machine:\s+(?:N\/A|({src_host}[^\s]+))""",
      """\sMachine IP:\s+(?:N\/A|({src_ip}[a-fA-F:\.\d]+))""",
      """\sFile Name:\s+(?:N\/A|({file_name}[^:]+?))\s*Machine IP:""",
      """\WSeverity:\s+({alert_severity}[^\s]+)""",
      """\sIncident ID:\s+({alert_id}\d+)""",
      """\sEndpoint Username:\s+(({domain}[^\\]+)\\)?({user}[^\s]+)""",
      """({alert_type}DLP ALERT)""",
    ]
    ParserVersion = "v1.0.0"
  

}
```