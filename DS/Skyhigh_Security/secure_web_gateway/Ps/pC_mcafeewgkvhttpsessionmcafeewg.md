#### Parser Content
```Java
{
Name = mcafee-wg-kv-http-session-mcafeewg
    Vendor = Skyhigh Security
    Product = Secure Web Gateway
    ParserVersion = "v1.0.0"
    TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
    Conditions = [ """McAfeeWG|""","""mwg:""" ]
    Fields = [
      """\|time_stamp=\[({time}[^\]]+)""",
      """\|server_ip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """\|auth_user=\s*(?:|({full_name}[^,|]+,[^|]+?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*\|""",
      """\|src_ip=(?:|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\|""",
      """\|host=(?:|({dest_host}[^|]+))\|""",
      """\|status_code=(?:|({http_response_code}\d+))\|""",
      """\|user_agent=(?:|({user_agent}[^|]+))\|""",
      """\|method=(?:|({method}[^|]+))\|""",
      """\|url=(-|({url}[^|]+?))\|""",
      """\|url=(?:|(\w+:\/+)?({web_domain}(?:({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|[^\/:|]+))[^|]*)\|""",
      """\|url=(?:|(\w+:\/+)?[^|\/:]+(:\d+)?({uri_path}\/[^?|]+)[^|]*)\|""",
      """\|url=(?:|(\w+:\/+)?[^|\/:]+(:\d+)?[^|?]+({uri_query}\?[^|]+))\|""",
      """\|categories=(?:|({category}[^,|]+))(,|\|)""",
      """\|bytes_to_client=(?:|({bytes_in}\d+))\|""",
      """\|bytes_from_client=(?:|({bytes_out}\d+))\|""",
      """\|block_reason=(?:|({failure_reason}[^|]+))\|""",
      """\|media_type=(?:|({mime}[^|]+?))\s*(\||$)"""
    ]
  

}
```