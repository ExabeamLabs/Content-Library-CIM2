#### Parser Content
```Java
{
Name = mcafee-wg-csv-http-session-getobserved
  Conditions = [""""Vendor:McAfee""",""","GET",""","""OBSERVED""" ]
  ParserVersion = "v1.0.0"

mcafee-http-session-2 = {
    Vendor = McAfee
    Product = McAfee Web Gateway
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy-MM-dd HH:mm:ss"]
    Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)\s({host}[\w\-.]+)\s(\S+\s+){4}"({user}[\w\.\-\!\#\^\~]{1,40}\$?)","({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))","({method}[^"]+)","({bytes_in}\d+)","({bytes_out}\d+)","(({url}[^?";]+)","({uri_path}\/[^;\?]*?)?)","({action}OBSERVED|PROXIED|DENIED)",("[^"]*",){3}"({protocol}[^"]+)","({categories}({category}[^,"]+?)(,[^"]*)?)",("[^"]*",){4}"({http_response_code}\d+)","({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",("[^"]*",){2}"({browser}[^"]+)","[^"]*","(\s*|({user_agent}[^"]+))""""
    """"({user}[\w\.\-\!\#\^\~]{1,40}\$?)","({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))","({method}GET|POST|PUT|TUNNEL|OPTIONS|CONNECT|HEAD|DELETE|CERTVERIFY)",""""
   """"(GET|POST|PUT|TUNNEL|OPTIONS|CONNECT|HEAD|DELETE|CERTVERIFY)","({bytes_in}\d+)","({bytes_out}\d+)","(({url}[^?";]+)","({uri_path}\/[^;\?]*?)?)","({action}OBSERVED|PROXIED|DENIED)","""
   """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)","({protocol}[^"]+)","({categories}({category}[^,"]+?)(,[^"]*)?)",("[^"]*",)""""
   """",("[^"]*",){6}"({http_response_code}\d+)","({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",("[^"]*",){2}"({browser}[^"]+)","[^"]*","(\s*|({user_agent}[^"]+))""""
    ]
    DupFields = ["url->web_domain"]
    
}
```