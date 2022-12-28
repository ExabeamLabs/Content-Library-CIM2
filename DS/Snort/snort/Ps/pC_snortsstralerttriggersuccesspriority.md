#### Parser Content
```Java
{
Name = snort-s-str-alert-trigger-success-priority
  Vendor = Snort
  Product = Snort
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """[Classification:""","""[Priority:""","""] [""" ]
  Fields = [
    """\[Classification:\s+({alert_type}[^\]]+)""",
    """\[Priority:\s+({alert_severity}[^\]]+)""",
    """\d+\]\s({alert_name}.+?)\s*(\s\S+\s)?\[Classification""",
    """Priority:[^:]+?\{(PROTO:)?({protocol}[^\}]+)\}""",
    """({src_ip}((\d{1,3}\.){3}\d{1,3}|[A-Fa-f\d]+:[a-fA-F\d:]+))(:({src_port}\d+))?\s*->\s*({dest_ip}((\d{1,3}\.){3}\d{1,3}|[A-Fa-f\d]+:[a-fA-F\d:]+))(:({dest_port}\d+))?"""
  ]


}
```