#### Parser Content
```Java
{
Name = mcafee-wg-kv-http-session-urlp-1
  ParserVersion = v1.0.0
  Vendor = McAfee
  Product = McAfee Web Gateway
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """mwg: """, """status="""", """srcip="""", """mtd="""", """urlp="""", """ua="""", """cache="""" ]
  Fields = [
    """mwg:\s({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """dhost="(-|({dest_host}[^"]+))""",
    """status="({http_response_code}\d+)""",
    """srcip="({src_ip}[a-fA-F\d:.]+)"""",
    """user="(-|({user}[^"]+))"""",
    """dstip="(-|({dest_ip}[a-fA-F\d:.]+))"""",
    """srcp="(-|({src_port}\d+))"""",
    """urlp="(-|({dest_port}\d+))""",
    """proto="(-|({protocol}[^"]+))"""",
    """\smtd="(-|({method}[^"]+))"""",
    """urlc="(-|({categories}[^"]+))"""",
    """urlc="(-|({category}[^",]+))""",
    """\smt="(-|({mime}[^"]+))"""",
    """app="(-|({app}[^"]+))"""",
    """bytes="(-|({bytes_in}\d+)\/({bytes_out}\d+)\/({bytes_in_post}\d+)\/({bytes_in_get}\d+))"""",
    """\sua="(_|({user_agent}[^"]+))"""",
    """rule="(-|({proxy_action}[^"]+))"""",
    """\surl="(-|({url}[^"]+))"""",
    """\surl="(?:[^:]+:\/+)((\d{1,3}\.){3}\d{1,3}|({web_domain}[^\/:\s"]+))""",
    """\surl="(-|\w+:\/+[^\/]+)({uri_path}\/[^?\s"]+)({uri_query}\?[^\s"]+)?""",
    """usrName ="(-|({user}[^"]+))""""
  ]
  

}
```