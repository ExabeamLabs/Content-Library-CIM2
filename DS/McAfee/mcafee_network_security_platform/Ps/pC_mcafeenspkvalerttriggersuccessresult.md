#### Parser Content
```Java
{
Name = mcafee-nsp-kv-alert-trigger-success-result
  Vendor = McAfee
  Product = McAfee Network Security Platform
  TimeFormat = "yyyy-MM-dd HH:mm:ss zzz"
  Conditions = [ """|Name:""" , """|Category:""", """|Application Protocol:""", """: Result:""" ]
  Fields = [
    """\|Time:\s*({time}[^\|]+)""",
    """\|Device:\s*({host}[\w\-.]+)\|""",
    """\|Name:\s*({protocol}[^\s:\|]+):\s*({alert_name}[^\|]+)""",
    """\|Category:\s*({alert_type}[^\|]+)""",
    """\|Severity:\s*({alert_severity}[^\|]+)""",
    """\|Application Protocol:\s*((?i)(n\/a)|({app_protocol}[^\|]+))""",
    """\|Destination IP:\s*({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\|Destination Port:\s*({dest_port}\d+)""",
    """\|Source IP:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\|Source Port:\s*({src_port}\d+)""",
    """Result:\s*((?i)(n\/a)|({result}[^\|]+))""",
  ]
  ParserVersion = "v1.0.0"


}
```