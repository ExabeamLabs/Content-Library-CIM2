#### Parser Content
```Java
{
Name = zeek-z-json-alert-trigger-success-weirdlog
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """/weird.log""", """"id.orig_h\":""", """"id.resp_h\":""", """"name\":""", """"peer\":""" ]
  Fields = [
    """"HOST"+:\s*"+({host}[^"]+)"""",
    """"TAGS"+:\s*"+({alert_type}[^"]+)"""",
    """"ts\\?"+:\\?"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})""",
    """"id\.orig_h\\?"+:\\?"+({src_ip}[a-fA-F\d.:]+)""",
    """"id\.orig_p\\?"+:({src_port}\d+)""",
    """"id\.resp_h\\?"+:\\?"+({dest_ip}[a-fA-F\d.:]+)""",
    """"id\.resp_p\\?"+:({dest_port}\d+)""",
    """"name\\?"+:\\?"+({alert_name}[^"\\]+)""",
    """"peer\\?"+:\\?"+({src_host}[^"\\]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```