#### Parser Content
```Java
{
Name = f5-waf-json-email-send-success-sentmail
  Conditions = [ """"log_type":"WAF"""", """"log_vendor":"f5"""", """ sSMTP[""", """]: Sent mail""" ]
  Fields = ${F5ParsersTemplates.f5-waf-activity.Fields} [
    """Sent mail for ({email_address}[^\s]+)""",
    """outbytes=({bytes}\d+)""",
    """uid=({message_id}[^\s]+)""",
    """username=({user}[^\s]+)"""
  ]
  ParserVersion = "v1.0.0"

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