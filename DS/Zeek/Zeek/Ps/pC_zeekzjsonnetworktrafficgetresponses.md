#### Parser Content
```Java
{
Name = zeek-z-json-network-traffic-getresponses
  Vendor = Zeek
  Product = Zeek 
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """/snmp.log""", """"get_requests\":""", """"get_responses\":""" ]
  Fields = [
    """"HOST"+:\s*"+({host}[^"]+)"""",
    """"TAGS"+:\s*"+({event_code}[^"]+)"""",
    """"ts\\?"+:\\?"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})""",
    """"uid\\?"+:\\?"+({connection_id}[^"\\]+)""",
    """"id\.orig_h\\?"+:\\?"+({src_ip}[a-fA-F\d.:]+)""",
    """"id\.orig_p\\?"+:({src_port}\d+)""",
    """"id\.resp_h\\?"+:\\?"+({dest_ip}[a-fA-F\d.:]+)""",
    """"id\.resp_p\\?"+:({dest_port}\d+)""",
    """"duration\\?"+:({duration}[\d\.]+)""",
    """"version\\?"+:\\?"+({version}[^"\\]+)""",
    """"community\\?"+:\\?"+({community}.+?)\\*"""",
# get_requests is removed
# get_bulk_requests is removed
# get_responses is removed
# set_requests is removed
  ]
  ParserVersion = "v1.0.0"


}
```