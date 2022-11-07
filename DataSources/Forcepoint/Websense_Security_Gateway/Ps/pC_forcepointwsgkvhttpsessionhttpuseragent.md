#### Parser Content
```Java
{
Name = forcepoint-wsg-kv-http-session-httpuseragent
    Vendor = Forcepoint
    Product = Websense Security Gateway
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ "vendor=Forcepoint","""http_user_agent=""","""http_proxy_status_code="""]
    Fields = [
      """({time}\d+-\d+-\d+T\d+:\d+:\d+[\+\-]\d+:\d+)""",
      """({host}\S+)\s+vendor=""",
      """\sdst_ip=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """\ssrc_host=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """\ssrc_port=({src_port}\d+)""",
      """\sdst_port=({dest_port}\d+)""",
      """user=.+?({user_ou}OU\\?=.+?)\s+(\w+=|$)""",
      """user=.+?DC\\?=\w+/(({email_address}[^@=\s]+@[^@=]+?)|({full_name}[^@=]+?)(@[^@=]*?)?)(\s+\w+=|\s*$)""",
      """\saction=({action}[^\s]+)""",
      """\shttp_method=(-|({method}[^\s]+))""",
      """\sbytes_in=({bytes_in}\d+)""",
      """\sbytes_out=({bytes_out}\d+)""",
      """\surl=(?:-|({url}[^\s"]+))""",
      """\surl=(?:-|({protocol}[^:]+))""",
      """\surl=([^:]+:\/+)?({web_domain}[^\s\/:]+).*?$""",
      """\surl=(?:-|\w+:\/+[^\s\/]+)({uri_path}\/[^?\s]*)""",
      """\surl=(?:-|(?=(?)(?:[^?]+({uri_query}\?[^\s"]+))))""",
      """\shttp_user_agent=(?:-|({user_agent}.+?))\s+http_proxy""",
      """\scategory=({category_id}.+?)\s+user""",
      """\shttp_content_type=(?:-|({mime}.+?))\s+http_""",
      """\shttp_proxy_status_code=({http_response_code}\d+)""",
      """\WloginID=(-|({user}[^\s]+))""",
    ]
        ParserVersion = "v1.0.0"
  

}
```