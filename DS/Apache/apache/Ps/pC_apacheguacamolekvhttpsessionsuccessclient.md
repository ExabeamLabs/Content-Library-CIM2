#### Parser Content
```Java
{
Name = apache-guacamole-kv-http-session-success-client
  Vendor = Apache
  Product = Apache
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ """ user="""", """ http_content_type="""", """ client=""", """ http_method="""", """ uri_path="""" ]
  Fields = [
    """time=({time}\d{10}\.\d+),""",
    """user="+(-|({user}[^"]+))"""",
    """http_method="+({method}[^"]+)"""",
    """server=({web_domain}[\w._-]+),""",
    """client=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """uri_path="+({uri_path}[^"]+)"""",
    """dest_port=({dest_port}\d+)""",
    """bytes_in=({bytes_in}\d+)""",
    """bytes_out=({bytes_out}\d+)""",
    """http_user_agent="+({user_agent}[^"]+)"""",
    """status=({http_response_code}\d+)""",
    """http_content_type="+(-|({mime}[^"]+))"""",
    """http_referrer="+(-|({referrer}[^"]+))"""",
    """uri_query="+\?({uri_query}[^"]+)""""
  ]


}
```