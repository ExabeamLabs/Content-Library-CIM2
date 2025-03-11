#### Parser Content
```Java
{
Name = fortinet-fortiweb-kv-http-session-traffic-http
  Vendor = Fortinet
  Product = Fortiweb Web Application Firewall
  TimeFormat = "epoch_sec"
  ParserVersion = "v1.0.0"
  Conditions = [ """type="traffic""", """subtype="http""", """proto=""", """status=""", """http_url="""", """http_method=""" ]
  Fields = [
    """timestamp=({time}\d{10})""",
    """devname="*({host}[^"\s]+)""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sdst=(0\.0\.0\.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """src_port=({src_port}\d+)""",
    """dst_port=({dest_port}\d+)""",
    """proto="*({protocol}[^\s"]+)""",
    """http_agent="(none|({user_agent}[^"]+))"\s\w+=""",
    """http_method=({method}[^=]+?)\s\w+=""",
    """http_request_bytes=({bytes_out}\d+)""",
    """http_response_bytes=({bytes_in}\d+)""",
    """user_name="(Unknown|({email_address}[^@"]+@[^\."]+\.[^"]+)|(({domain}[^\\"]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """http_refer="(none|({referrer}[^"]+))""",
    """http_url="*(\w+:\/{2})?[^\/]+({uri_path}\/[^?\s"]+)?(\?({uri_query}[^"]+))?"""",
    """http_retcode=({http_response_code}\d+)""",
    """msg="({additional_info}[^"=]+)"\s\w+="""
  ]


}
```