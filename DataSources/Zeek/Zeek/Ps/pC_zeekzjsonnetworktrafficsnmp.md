#### Parser Content
```Java
{
Name = zeek-z-json-network-traffic-snmp
  Product = Zeek
  Vendor = Zeek
  TimeFormat = "epoch_sec"
  Conditions = [ """ zeek_snmp """, """id.""", """"get_requests"""", """"get_responses"""" ]
  Fields = [
    """"ts\\?"+:({time}\d{10})""",
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