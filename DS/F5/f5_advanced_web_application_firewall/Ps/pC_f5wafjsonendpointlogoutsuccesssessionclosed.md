#### Parser Content
```Java
{
Name = f5-waf-json-endpoint-logout-success-sessionclosed
  ParserVersion = v1.0.0
  Conditions = [ """"log_type":"WAF"""", """"log_vendor":"f5"""", """sshd[""", """]: """, """session closed for user""" ]
  Fields = ${F5DLParsersTemplates.f5-waf-activity.Fields} [
    """(({event_name}session closed for user) ({user}[^"\s]+))""",
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