#### Parser Content
```Java
{
Name = "f5-bigipdns-mix-http-request-http"
  Vendor = "F5"
  Product = "F5 BIG-IP DNS"
  ParserVersion = "v1.0.0"
  TimeFormat = ["dd/MMM/yyyy HH:mm:ss Z", "MMM dd HH:mm:ss"]
  Conditions = [ """ <HTTP_REQUEST>""", """]: """ ]
  Fields = [
    """({time}\w+ \d+ \d+:\d+:\d+)\s+"""
    """\w+ \d+ \d\d:\d\d:\d\d ({host}[\w\-.]+) ({event_category}[^:]+?)\s+\w+\[\d+\]:\s*[^:]*?\s+({rule}[^:]+?) <HTTP_REQUEST>:?[\-\s]*([^=]*?)\s+$""", # rule_response is removed
    """for blocking decision is ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """date_time=\[({time}\d\d\/\w+\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(-|\+)\d+)\]""",
    """\svs_name=({action}[^=]+?)\s+\w+=""",
    """\d\d:\d\d:\d\d\s+({host}[\w.-]+)\s({event_category}\w+)\s""",
    """method=({method}[^\s]+)""",
    """:\s+Rule\s+({rule}[^\s]+)""",
    """client_ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """client_port=({src_port}\d+)""",
    """v_ip=({src_translated_ip}[A-Za-z0-9.:]+)""",
    """v_port=({src_translated_port}\d+)""",
    """path=({uri_path}[^=]+)\s+\w+=""",
    """query=({uri_query}[^\s]+)\s+\w+=""",
    """dest_host=({web_domain}[^\s]+)""",
    """user_agent="({user_agent}[^"=]+)"""",
    """user_agent="({browser}[^\/";]+)[^"]+?({os}iOS|Android|BlackBerry|Windows Phone|BeOS|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin)"""
  ]


}
```