#### Parser Content
```Java
{
Name = forcepoint-wsg-leef-http-session-security
    Vendor = Forcepoint
    Product = Websense Security Gateway
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """LEEF:""","""|Forcepoint|Security|""","""|transaction:""","""srcBytes=""" ]
    Fields = [
      """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """\ssrcPort=({src_port}\d+)""",
      """\sdstPort=({dest_port}\d+)""",
      """\susrName =(?:\w+:\/+\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s+({user_ou}[^\/]+)\/({full_name}.+?)\s+([\w\-]+=|$)""",
      """\sloginID=(-|(({domain}[^=]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)""",
      """\|transaction:({action}[^\|]+)""",
      """\smethod=(?:-|({method}[^\s]+))""",
      """\ssrcBytes=({bytes_in}\d+)""",
      """\sdstBytes=({bytes_out}\d+)""",
      """\surl=(?:-|({url}[^\s"]+))""",
      """\surl=(?:-|({protocol}[^:]+))""",
      """\surl=(?:[^:]+:\/+)({web_domain}[^\/:\s"]+)""",
      """\surl=(?:-|\w+:\/+[^\/]+)({uri_path}\/[^?\s"]+)""",
      """\surl=(?:-|(?=(?)(?:[^?]+({uri_query}\?[^\s"]+))))""",
      """\suserAgent=(?:-|({user_agent}.+?))\s+url=""",
      """\scontentType=(?:-|({mime}.+?))\s+reason=""",
      """\sproxyStatus-code=({http_response_code}\d+)""",
      """cat=({category_id}\d+)""",
    ]
	ParserVersion = "v1.0.0"
  

}
```