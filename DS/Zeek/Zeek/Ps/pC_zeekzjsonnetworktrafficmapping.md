#### Parser Content
```Java
{
Name = zeek-z-json-network-traffic-mapping
  Vendor = Zeek
  Product = Zeek 
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """/smb_mapping.log""", """"id.orig_h\":""", """"id.resp_h\":""", """"share_type\":""" ]
  Fields = [
    """"HOST"+:\s*"+({host}[^"]+)"""",
    """"TAGS"+:\s*"+({event_code}[^"]+)"""",
    """"ts\\?"+:\\?"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})""",
    """"uid\\?"+:\\?"+({connection_id}[^"\\]+)""",
    """"id\.orig_h\\?"+:\\?"+({src_ip}[a-fA-F\d.:]+)""",
    """"id\.orig_p\\?"+:({src_port}\d{1,100})""",
    """"id\.resp_h\\?"+:\\?"+({dest_ip}[a-fA-F\d.:]+)""",
    """"id\.resp_p\\?"+:({dest_port}\d+)""",
    """"path\\?"+:\\?"+({share_path}[^"]+)""",
    """"share_type\\?"+:\\?"+({share_type}[^"\\]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```