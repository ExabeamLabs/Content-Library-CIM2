#### Parser Content
```Java
{
Name = fortinet-fortiweb-kv-http-session-threatweight
  Vendor = Fortinet
  Product = Fortiweb Web Application Firewall
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """action=""", """service=""", """app_name=""", """threat_weight=""", """main_type=""" ]
  Fields = [
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+(\+|-)\d\d:\d\d)""",
    """http_host=(none|({web_domain}[^\s]+))""",
    """src_ip=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """dst_port=({dest_port}\d{1,5})""",
    """src_port=({src_port}\d{1,5})""",
    """http_agent=(none|-|({user_agent}[^"]+?))\s+http_refer=""",
    """http_method=(NONE|({method}[^=]+?))\s\w+=""",
    """user_name=+(({email_address}[^\s@]+@[^\s@]+)|({user}[^\s]+))""",
    """http_refer=(none|({referrer}[^=]+?))\s\w+=""",
    """http_url=(none|(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({url}(({protocol}[^:\\\/\s,"]+):[\\\/]+)?({web_domain}[^\\\/\s:,"]+)?({uri_path}\/[^\s\?"]*)?({uri_query}\?[^"\s]*)?)))"""
    """app_name="({app}[^"]+)""",
    """action=({action}[^\s]+)""",
  ]


}
```