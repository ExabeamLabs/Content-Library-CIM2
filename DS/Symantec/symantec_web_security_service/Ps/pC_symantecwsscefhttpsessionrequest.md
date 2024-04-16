#### Parser Content
```Java
{
Name = symantec-wss-cef-http-session-request
  ParserVersion = v1.0.0 
  Vendor = Symantec
  Product = Symantec Web Security Service
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy-MM-dd HH:mm:ss"]
  Conditions = [
"""requestClientApplication=Symantec WSS"""
  ]
  Fields = [
    """({action}OBSERVED|PROXIED|DENIED),"*\s*({category}.+?)"*,\s(?:-|({referrer}.+?))\s*,\s(?:-|({http_response_code}\d+)),\s(?:-|unknown|({proxy_action}[^,]+)),\s""",
    """, ({action}OBSERVED|PROXIED|DENIED),([^,]+,){1}(\s*-,\s|(.+?,\s))([^,]+,){2}\s*(?:-|unknown|({method}(GET|POST|PUT|TUNNEL|OPTIONS|CONNECT|HEAD|DELETE))),\s*(?:-|({mime}[^,]+)),\s(?:-|({protocol}[^,]+)),\s({url}[^\s]+?),\s(?:-|({dest_port}\d+)),\s(?:-|({uri_path}[^\s]+?))\s*,\s(-|({uri_query}[^\s]+?)),([^,]+,){1}\s({user_agent}[^-]+?),\s\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}"""
    """, ({action}OBSERVED|PROXIED|DENIED),([^,]+,){1}(\s*-,\s|(.+?,\s))([^,]+,){2}\s*(?:-|unknown|({method}(GET|POST|PUT|TUNNEL|OPTIONS|CONNECT|HEAD|DELETE))),\s*(?:-|({mime}[^,]+)),\s(?:-|({protocol}[^,]+)),\s({url}[^\s]+?),\s(?:-|({dest_port}\d+)),\s(?:-|({uri_path}[^\s]+?))\s*,\s(-|({uri_query}[^\s]+?)),"""
    """, ({action}OBSERVED|PROXIED|DENIED),([^,]+,){4}\s*(?:-|unknown|({method}(GET|POST|PUT|TUNNEL|OPTIONS|CONNECT|HEAD|DELETE))),\s*(?:-|({mime}[^,]+)),\s(?:-|({protocol}[^,]+)),\s({url}[^,]+),\s(?:-|({dest_port}\d+)),\s(?:-|({uri_path}[^,]+))\s*,\s(-|({uri_query}[^,]+)),"""
    """,\s*({user_agent}(iOS|Android|BlackBerry|Microsoft|Windows Phone|BeOS|(?:X|x)11|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin|Chrome|Safari|Opera|(?:F|f)irefox|MSIE|Trident|Mozilla|Breakpad)[^,]+),"""
    """cs6=.+?({time}\d\d\d\d-\d\d-\d\d,?\s\d\d:\d\d:\d\d)"""
    """({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z)""",
    """\sproto=({protocol}\d+)""",
    """\ssuid=(anonymous|({user_uid}[^\s]+))""",
    """\ssuser=(({domain}[^\\\s]+)\\+)?(anonymous|system-process|({user}[\w\.\-]{1,40}\$?))""",
    """\Wsuser=(({domain}[^\\\s]+)\\+)?(non-interactive-user|anonymous|system-process({user}[\w\.\-]{1,40}\$?))""",
    """\sapp=({category}.+?)\s\w+=""",
    """\sdhost=({web_domain}.+?)\s\w+=""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s*(\w+=|$)""",
    """\sflexString1=({proxy_action}.+?)\s\w+=""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s*(\w+=|$)""",
    """\Wdproc=(|({process_name}.+?))(\s+\w+=|\s*$)""",
    """\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s(({domain}[^\s\\]+)\\)?({user}[\w\.\-]{1,40}\$?)\s(\S+\s){2}({action}OBSERVED)\s"({categories}({category}[^"]+)[^,"]*)"\s(-|({referrer}[^\s]+))\s({http_response_code}\d{1,100})\s(-|({proxy_action}[^\s]+))\s({method}[^\s]+)\s(-|({mime}[^\s]+))\s({protocol}[^\s]+)\s({web_domain}[^\s]+)\s({dest_port}\d{1,100})\s({uri_path}\S+?)?\s(-|({uri_query}\?[^\s]*?)?)\s\S+\s(none|-|"({user_agent}[^"]+)")\s(\d{1,3}\.){3}\d{1,3}\s({bytes_out}\d{1,100})\s({bytes_in}\d{1,100})\s"""
  ]
  

}
```