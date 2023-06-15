#### Parser Content
```Java
{
Name = fortinet-fortiedr-kv-alert-trigger-success-ensilo
  Vendor = Fortinet
  Product = EnSilo
  TimeFormat = "dd-MMM-yyyy', 'HH:mm:ss"
  Conditions = [ """ enSilo """, """;Raw Data ID:""", """;Rules List:""", """;Severity:""" ]
  Fields = [
    """\s({host}[\w\-.]+)\s+enSilo""",
    """\WFirst Seen:\s*({time}\d+-\w+-\d+,\s*\d+:\d+:\d+)""",
    """\WEvent ID:\s*({event_code}[^;]+)""",
    """\WRaw Data ID:\s*({alert_id}[^;]+)""",
    """\WDevice Name:\s*({src_host}[\w\-.]+)""",
    """\WProcess Name:\s*({process_name}[^;]+)""",
    """\WProcess Path:\s*({process_path}[^;]+)""",
    """\WProcess Type:\s*({process_type}[^;]+)""",
    """\WSeverity:\s*({alert_severity}[^;]+)""",
    """\WClassification:\s*({category}[^;]+)""",
    """\WRules List:\s*({alert_type}[^;]+)""",
    """\WDestination:\s*(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))|({alert_type}[^;]+));""",
    """\WAction:\s*({action}[^;]+)""",
    """\WCount:\s*({rule_count}\d+)""",
    """\WRules List:\s*({alert_name}[^;]+)""",
    """\WUsers:\s*(({domain}[^\\\s;]+)\\+)?({user}[^\\\s;]+)""",
    """\WMAC Address:\s*({src_mac}[^;,\s]+)""",
   ]
   ParserVersion = "v1.0.0"


}
```