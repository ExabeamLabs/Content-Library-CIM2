#### Parser Content
```Java
{
Name = f5-waf-json-email-send-success-sentmail
  Conditions = [ """"log_type":"WAF"""", """"log_vendor":"f5"""", """ sSMTP[""", """]: Sent mail""" ]
  Fields = ${F5ParsersTemplates.f5-waf-activity-aa.Fields} [
    """Sent mail for ({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """outbytes=({bytes}\d+)""",
    """uid=({message_id}[^\s]+)""",
    """username=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  ]
  ParserVersion = "v1.0.0"

f5-waf-activity-aa = {
    Vendor = F5
    Product = F5 Advanced Web Application Firewall
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""",
      """"host":"(::ffff:)?({host}[^"]+)""",
      """\d\d:\d\d:\d\d ({host}[^\s]+) \w+ \w+\["""
    
}
```