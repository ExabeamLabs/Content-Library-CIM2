#### Parser Content
```Java
{
Name = suricata-s-str-alert-trigger-success-classification
  Vendor = Suricata
  Product = Suricata
  TimeFormat = "MMM dd HH:mm:ss"
  Conditions = [ """ suricata[""", """ [Classification:""", """] [Priority:""" ]
  Fields = [
    """({time}\w{3}\s+\d{1,2}\s\d\d:\d\d:\d\d)\s({host}[\w\-.]+)\ssuricata""",
    """suricata\[[^\[]+\[(({event_code}[^\]]+))""",
    """\[Classification:\s*({alert_type}[^\]]+)\]""",
    """\[Priority:\s*({alert_severity}[^\]]+)\]""",
    """\d+\]\s({alert_reason}({alert_name}[^\[\(]+)(\s\([^\[]*)?)\s+\[Classification""",
    """\[Priority:[^:]+?\{(PROTO:)?({protocol}[^\}]+)\}""",
    """\s(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|[A-Fa-f\d]+:[a-fA-F\d:]+))(:({src_port}\d+))?\s*->\s*(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|[A-Fa-f\d]+:[a-fA-F\d:]+))(:({dest_port}\d+))?"""
  ]
  ParserVersion = v1.0.0


}
```