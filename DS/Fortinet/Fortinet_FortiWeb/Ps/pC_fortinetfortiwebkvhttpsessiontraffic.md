#### Parser Content
```Java
{
Name = fortinet-fortiweb-kv-http-session-traffic
  Vendor = Fortinet
  Product = Fortinet FortiWeb
  TimeFormat = "yyyy-MM-dd' time='HH:mm:ss"
  Conditions = [ """proto=tcp""", """type=traffic""", """original_src=""", """content_switch_name=""", """service=""", """user_name="""", """http_url="""", """pri=""", """http_method=""" ]
  Fields = [
    """\Wdate=({time}\d\d\d\d-\d\d-\d\d time\=\d\d:\d\d:\d\d)""",
    """http_host="(none|({host}[a-fA-F:\d\.]+):\d+|({=host}[^"]+))""",
    """\ssrc=({src_ip}[a-fA-F\d\.:]+)""",
    """\sdst=(0\.0\.0\.0|({dest_ip}[a-fA-F\d\.:]+))""",
    """src_port=({src_port}\d+)""",
    """dst_port=({dest_port}\d+)""",
    """proto=({protocol}[^\s]+)""",
    """http_agent="(none|({user_agent}[^"]+))"\s\w+=""",
    """http_method=({method}[^=]+?)\s\w+=""",
    """http_request_bytes=({bytes_out}\d+)""",
    """http_response_bytes=({bytes_in}\d+)""",
    """user_name="(Unknown|(({domain}[^\\]+)\\)?({user}[^"]+))""",
    """http_refer="(none|({referrer}[^"]+))""",
    """http_url="*(\w+:\/{2})?[^\/]+({uri_path}\/[^?\s"]+)?(\?({uri_query}[^"]+))?"""",
    """http_retcode=({http_response_code}\d+)"""
  ]
  ParserVersion = "v1.0.0"


}
```