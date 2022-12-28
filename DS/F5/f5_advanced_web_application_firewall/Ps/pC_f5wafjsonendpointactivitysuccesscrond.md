#### Parser Content
```Java
{
Name = f5-waf-json-endpoint-activity-success-crond
  ParserVersion = v1.0.0
  Conditions = [ """"log_type":"WAF"""", """"log_vendor":"f5"""", """crond[""", """]: """ ]
  Fields = ${F5DLParsersTemplates.f5-waf-activity.Fields} [
    """\d\d:\d\d:\d\d ({host}\S+) crond\[""",
    """\scrond\[\d+\]:\s*({additional_info}[^=]+?)\s*$"""
  ]

f5-waf-activity = {
    Vendor = F5
    Product = F5 Advanced Web Application Firewall
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Fields = [
      """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
      """"host":"(::ffff:)?({host}[^"]+})""",
      """\d\d:\d\d:\d\d ({host}\S+)? \w+ \w+\[""",
      """\ssshd\[\d+\]:\s*({additional_info}[^",]+)"""
    
}
```