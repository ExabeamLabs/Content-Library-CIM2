#### Parser Content
```Java
{
Name = cisco-fp-str-alert-trigger-success-impact
  Vendor = Cisco
  Product = Cisco Firepower
  TimeFormat = "MMM dd HH:mm:ss yyyy z"
  Conditions = [ """[Classification:""", """[Priority:""", """[Impact:""", """message":"[""" ]
  Fields = [
    """(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+\s+\d+\s+\d\d:\d\d:\d\d \d\d\d\d \w+)""",
    """\[({alert_name}\d+:\d+:\d+)\]""",
    """\[Classification:\s*({alert_type}[^\]]+)\]""",
    """\[Priority:\s*({alert_severity}\d+)\] \{({protocol}[^\}]+)\}""",
    """\[\d+:\d+:\d+\]\s+\*"({additional_info}[^"]+?)\*"""",
    """\{\w+\}\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\:+({src_port}\d+) \((unknown|({src_country}[^\)]+))""",
    """->\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\:+({dest_port}\d+) \((unknown|({dest_country}[^\)]+))""",
    """\[Impact:\s*(Unknown|({impact}[^\]]+))""",
    """ From \"({src_host}[\w\-.]+)\"""",
  ]
  ParserVersion = "v1.0.0"


}
```