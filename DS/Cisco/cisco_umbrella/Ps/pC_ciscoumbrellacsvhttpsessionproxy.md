#### Parser Content
```Java
{
Name = cisco-umbrella-csv-http-session-proxy
  Vendor = Cisco
  Product = Cisco Umbrella
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  ParserVersion = "v1.0.0"
  Conditions = [ """destinationServiceName =CiscoUmbrella """, """dproc=Proxy """ ]
  Fields = [
    """destinationServiceName =({app}[^=]+?)\s+\w+=""",
    """>\s*("[^"]*",){7}"({protocol}http(s)?)"""
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)","({dest_host}[\w\-\.]+)","({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))","[^"]+","({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?","({mime}[^",]+)","({action}[^",]+)","({url}[^",]+)","({referrer}[^",]+)","({user_agent}[^"]+)","({http_response_code}\d+)","({bytes_in}\d+)?","({bytes_out}\d+)?","[^"]*","({hash_sha256}[^"]+)","({categories}({category}[^,"]+)?(\s*,[^"]*?)?)(?:",)?",("[^"]*",){8}"({identity_type}[^"]+)","({method}[^"]+)","""
  ]


}
```