#### Parser Content
```Java
{
Name = zeek-z-json-dhcp-traffic-success-uids
  Vendor = Zeek
  Product = Zeek 
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """/dhcp.log""", """"uids\":""" ]
  Fields = [
    """"HOST"+:\s*"+({host}[^"]+)"""",
    """"TAGS"+:\s*"+({event_code}[^"]+)"""",
    """"ts\\?"+:\\?"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})""",
    """"client_addr\\?"+:\\?"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"server_addr\\?"+:\\?"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"mac\\?"+:\\?"+({src_mac}[^"\\]+)""",
    """"host_name\\?"+:\\?"+({src_host}[^"\\]+)""",
    """"client_fqdn\\?"+:\\?"+({domain}[^"\\]+)""",
    """"domain\\?"+:\\?"+({domain}[^"\\]+)""",
# requested_addr is removed
    """"assigned_addr\\?"+:\\?"+({assigned_ip}[a-fA-F\d.:]+)""",
    """"lease_time\\?"+:({lease_time}\d+)""",
    """"msg_types\\?"+:\[({category}.+?)\]""",
    """"duration\\?"+:\s*({duration}(-)?[\d\.]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```