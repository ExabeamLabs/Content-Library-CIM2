#### Parser Content
```Java
{
Name = extrahop-revealx-json-alert-trigger-success-sec
  Vendor = Extrahop
  Product = Extrahop Reveal(x)
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """categories""", """sec.""", """vendor":"ExtraHop""", """description""","""title"""]
  Fields = [
     """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+-\d+:\d+)\s*({host}[^\s]+)""",
     """"description":"({additional_info}[^"]+)""", 
     """"ipaddrs":\["({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?.+?offender""",
     """"ipaddrs":\["({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?.+?victim""",
     """"dnsNames":\["({src_host}[^."]+)(\.({domain}[^"]+))?".+?offender""",
     """"dnsNames":\["({dest_host}[^."]+)(\.({domain}[^"]+))?".+?victim""",
     """"title":"({alert_name}[^"]+)""",
     """"netbiosName":(null|"({sub_domain}[^"]+))""",
     """"dnsNames":\["({dns_query}[^"]+)"\]""",
     """"status":(null|"({status_msg}[^"\s]+))""",
     """"riskScore":(null|({original_risk_score}\d+))""",
  ]
  DupFields = ["alert_name->alert_type",
  "original_risk_score->alert_severity"]
  ParserVersion = "v1.0.0"


}
```