#### Parser Content
```Java
{
Name = f5-waf-json-endpoint-logout-success-connectionclosed
  ParserVersion = v1.0.0
  Conditions = [ """"log_type":"WAF"""", """"log_vendor":"f5"""", """ sshd[""", """Connection closed by""" ]
  Fields = ${F5DLParsersTemplates.f5-waf-activity.Fields} [
    """Connection closed by ({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+port\s+({src_port}\d+)"""
  ]

f5-waf-activity = {
    Vendor = F5
    Product = F5 Advanced Web Application Firewall
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""",
      """"host":"(::ffff:)?({host}[^"]+})""",
      """\d\d:\d\d:\d\d ({host}\S+)? \w+ \w+\[""",
      """\ssshd\[\d+\]:\s*({additional_info}[^",]+)"""
    
}
```