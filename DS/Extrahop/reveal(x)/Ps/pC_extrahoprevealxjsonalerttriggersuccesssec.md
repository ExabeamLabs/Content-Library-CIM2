#### Parser Content
```Java
{
Name = extrahop-revealx-json-alert-trigger-success-sec
  Vendor = Extrahop
  Product = Reveal(x)
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS-SS:SS"
  Conditions = [ """categories""", """sec.""", """vendor":"ExtraHop""", """description""","""title"""]
  Fields = [
     """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+-\d+:\d+)\s*({host}[^\s]+)""",
     """"description":"({additional_info}[^"]+)""", 
     """"ipaddrs":\["({src_ip}[A-Fa-f:\d.]+).+?offender""",
     """"ipaddrs":\["({dest_ip}[A-Fa-f:\d.]+).+?victim""",
     """"dnsNames":\["({src_host}[^."]+)(\.({domain}[^"]+))?".+?offender""",
     """"dnsNames":\["({dest_host}[^."]+)(\.({domain}[^"]+))?".+?victim""",
     """"title":"({alert_name}[^"]+)""",
     """"netbiosName":(null|"({sub_domain}[^"]+))""",
     """"dnsNames":\["({query}[^"]+)"\]""",
     """"status":(null|"({status}[^"\s]+))""",
     """"riskScore":(null|({alert_severity}\d+))""",
  ]
  DupFields = ["alert_name->alert_type"]
  ParserVersion = "v1.0.0"


}
```