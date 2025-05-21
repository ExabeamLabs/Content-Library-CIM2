#### Parser Content
```Java
{
Name = symantec-dlp-kv-alert-trigger-success-dlpalert
    Vendor = Symantec
    Product = Symantec DLP
    TimeFormat = ["dd MMM yyyy hh:mm:ss a","dd MMM yyyy HH:mm:ss"]
    Conditions = [ """Policy Violated: """, """Endpoint Machine: """, """DLP ALERT""", """Application Name: """, """Incident ID: """ ]
    Fields = [
      """\d\d:\d\d:\d\d\s+({host}[^\s]+)"""
      """Reported On:\s+({time}\d{0,2} \w+ \d{1,4} \d{0,2}:\d{0,2}:\d{0,2} (am|pm|PM|AM))"""
      """\sPolicy Violated:\s+({alert_name}[^:]+?)\s*Reported On:""",
      """({additional_info}DLP ALERT|DLP ALERT[^:]+?)\s+Application Name:""",
      """\sApplication Name:\s+({app}[^:]+?)\s*Endpoint Machine:"""
      """\WEndpoint Machine:\s+(?:N\/A|({src_host}[^\s]+))""",
      """\sMachine IP:\s+(?:N\/A|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
      """\sFile Name:\s+(?:N\/A|({file_name}[^:]+?))\s*Machine IP:""",
      """\WSeverity:\s+({alert_severity}[^\s]+)""",
      """\sIncident ID:\s+({alert_id}\d+)""",
      """\sEndpoint Username:\s+(({domain}[^\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
      """({alert_type}DLP ALERT)""",
    ]
    ParserVersion = "v1.0.0"
  

}
```