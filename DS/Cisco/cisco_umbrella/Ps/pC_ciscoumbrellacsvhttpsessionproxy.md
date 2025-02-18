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
    """>\s*("[^"]*",){7}"({protocol}http(s)?)""",
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)","({full_name}[^\(]+?)\s\(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^"]+\.[^"]+)\)(,({host}[^"]+))?","(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))","[^"]+","(|(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?))".*?"AD Users,(Anyconnect Roaming Client|Roaming Computers)""""
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)","({dest_host}[\w\-\.]+)","(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))","[^"]+","(|(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?))""""
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)","({src_host}[\w\-\.]+)","(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))","[^"]+","(|(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?))".*?(Anyconnect Roaming Client|Roaming Computers)""""
    """(\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)",("[^"]*",){4}"(|({mime}[^",]+))","({action}[^",]+)","({url}[^"]*?)","(|({referrer}[^"]+))","\s*({user_agent}[^"]+)?","({http_response_code}\d+)","({bytes_in}\d+)?","({bytes_out}\d+)?","[^"]*","(|({hash_sha256}[^"]+))","({categories}({category}[^,"]+)?(\s*,[^"]*?)?)(?:",)?",("[^"]*",){8}"({identity_type}[^"]+)","({method}[^"]+)","""
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)",("[^"]*",){4}"(|({mime}[^",]+))","({action}[^",]+)","({url}[^"]*?)","(|({referrer}[^"]+))","\s*({user_agent}[^"]+)?","({http_response_code}\d+)","({bytes_in}\d+)?","({bytes_out}\d+)?","[^"]*","(|({hash_sha256}[^"]+))","({categories}({category}[^,"]+)?(\s*,[^"]*?)?)(?:",)?",("[^"]*",){7}"({src_host}[\w\-\.]+),({full_name}[^\(]+?)\s\(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^"]+\.[^"]+)\)","({identity_type}(Anyconnect Roaming Client,AD Users|Roaming Computers,AD Users))","({method}[^"]+)"""
  ]


}
```