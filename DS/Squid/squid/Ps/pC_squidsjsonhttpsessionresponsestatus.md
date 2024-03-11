#### Parser Content
```Java
{
Name = squid-s-json-http-session-responsestatus
  ParserVersion = v1.0.0
  Vendor = Squid
  Product = Squid
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [
"""http_method"""
"""http_status_code"""
"""squid_request_status"""
]
  Fields = [
    """timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """http_username":"(-|({user}[^"]+))"""",
    """http_method":"({method}[^"]+)"""",
    """squid_request_status":"({proxy_action}[^"]+)"""",
    """http_url":"(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({url}(({protocol}[^:\\\/\s,"]+):[\\\/]+)?({web_domain}[^\\\/\s:,"]+)?({uri_path}\/[^\s\?"]*)?({uri_query}\?[^"\s]*)?))""",
    """http_status_code"*:({http_response_code}\d+)""",
    """ip_server":"(-|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""",
    """ip_client":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """http_reply_size":({bytes_out}\d+)""",
    """http_received_size":({bytes_in}\d+)""",
    """http_mime_type":"(-|({mime}[^"]+?))","""
  ]


}
```