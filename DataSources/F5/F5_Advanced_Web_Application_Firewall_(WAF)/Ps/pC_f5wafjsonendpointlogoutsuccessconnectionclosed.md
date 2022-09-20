#### Parser Content
```Java
{
Name = f5-waf-json-endpoint-logout-success-connectionclosed
  ParserVersion = v1.0.0
  Conditions = [ """"log_type":"WAF"""", """"log_vendor":"f5"""", """ sshd[""", """Connection closed by""" ]
  Fields = ${F5DLParsersTemplates.f5-waf-activity.Fields} [
    """Connection closed by ({src_ip}[A-Fa-f.:\d]+)\s+port\s+({src_port}\d+)"""
  ]

f5-waf-activity = {
    Vendor = F5
    Product = F5 Advanced Web Application Firewall (WAF)
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Fields = [
      """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
      """"host":"(::ffff:)?({host}[^"]+})""",
      """\d\d:\d\d:\d\d ({host}\S+)? \w+ \w+\[""",
      """\ssshd\[\d+\]:\s*({additional_info}[^",]+)"""
    
}
```