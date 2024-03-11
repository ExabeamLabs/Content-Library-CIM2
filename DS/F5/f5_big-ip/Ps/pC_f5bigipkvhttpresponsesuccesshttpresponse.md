#### Parser Content
```Java
{
Name = f5-bigip-kv-http-response-success-httpresponse
  ParserVersion = v1.0.0
  Vendor = F5
  Product = F5 BIG-IP
  TimeFormat = "dd/MMM/yyyy HH:mm:ss Z"
  Conditions = [ """<HTTP_RESPONSE>:""", """date_time=""", """client_ip=""", """client_port=""", """status_code=""", """method=""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s+({host}[\w.-]+)\s\w+""",
    """date_time=\[({time}\d\d\/\w+\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(-|\+)\d+)\]""",
    """client_ip=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """client_port=({src_port}\d+)""",
    """status_code=({http_response_code}\d+)""",
    """method=({method}[^\s]+)""",
    """dest_host=({web_domain}[^\s]+)""",
    """dest_host=[^\=\s]*?({top_domain}[^\/\.\s]+(?:\.(?:com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za|ms))+)\s+\w+=""",
    """path=({uri_path}[^=]+)\s+\w+=""",
    """query=({uri_query}[^\s]+)\s+\w+=""",
    """server_ip=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """server_port=({dest_port}\d+)""",
    """snat_ip=({src_translated_ip}[A-Za-z0-9.:]+)""",
    """snat_port=({src_translated_port}\d+)""",
    """user_agent="({user_agent}[^"=]+)"""",
    """user_agent="({browser}[^\/";]+)[^"]+?({os}iOS|Android|BlackBerry|Windows Phone|BeOS|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin)"""
  ]


}
```