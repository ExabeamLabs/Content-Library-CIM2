#### Parser Content
```Java
{
Name = mcafee-wg-kv-http-session-mcafeewg
    Vendor = McAfee
    Product = McAfee Web Gateway
    ParserVersion = "v1.0.0"
    TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
    Conditions = [ """McAfeeWG|""","""mwg:""" ]
    Fields = [
      """\|time_stamp=\[({time}[^\]]+)""",
      """\|server_ip=({dest_ip}[^|]+)""",
      """\|auth_user=(?:|({user}[^|]+))\|""",
      """\|src_ip=(?:|({src_ip}[^|]+))\|""",
      """\|host=(?:|({dest_host}[^|]+))\|""",
      """\|status_code=(?:|({http_response_code}\d+))\|""",
      """\|user_agent=(?:|({user_agent}[^|]+))\|""",
      """\|method=(?:|({method}[^|]+))\|""",
      """\|url=(-|({url}[^|]+?))\|""",
      """\|url=(?:|(\w+:\/+)?({web_domain}(?:({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|[^\/:|]+))[^|]*)\|""",
      """\|url=(?:|(\w+:\/+)?[^|\/:]+(:\d+)?({uri_path}\/[^?|]+)[^|]*)\|""",
      """\|url=(?:|(\w+:\/+)?[^|\/:]+(:\d+)?[^|?]+({uri_query}\?[^|]+))\|""",
      """\|categories=(?:|({event_category}[^,|]+))(,|\|)""",
      """\|bytes_to_client=(?:|({bytes_in}\d+))\|""",
      """\|bytes_from_client=(?:|({bytes_out}\d+))\|""",
      """\|block_reason=(?:|({failure_reason}[^|]+))\|""",
      """\|media_type=(?:|({mime}[^|]+?))\s*(\||$)"""
    ]
  

}
```