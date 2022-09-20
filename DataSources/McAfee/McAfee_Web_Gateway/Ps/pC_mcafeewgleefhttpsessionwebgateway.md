#### Parser Content
```Java
{
Name = mcafee-wg-leef-http-session-webgateway
    Vendor = McAfee
    Product = McAfee Web Gateway
	ParserVersion = "v1.0.0"
    TimeFormat = "epoch"
    Conditions = [ """LEEF:""","""|McAfee|Web Gateway|""" ]
    Fields = [
                """\|devTime=({time}\d+)""",
                """\d\d:\d\d:\d\d\s({host}[^\s]+)\s(mwg:\s)?LEEF:""",
                """\|usrName =(?:|({user}[^|]+))\|""",
                """\|src=(?:|({src_ip}[^|]+))\|""",
                """\|dst=(?:|({dest_ip}[^|]+))\|""",
                """\|httpStatus=(?:|({http_response_code}\d+))\|""",
                """\|Prot=(?:|({protocol}[^|]+))\|""",
                """\|(?:agent|usrAgent)=(?:|({user_agent}[^|]+))\|""",
                """\|Meth=(?:|({method}[^|]+))\|""",
                """\|url=(-|({url}.+?))(\|\w+=|\"|\s*$|$)""",
                """\|url=(?:|(\w+:\/+)?({web_domain}(?:({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|[^\/:|]+))[^|]*)(\||\"|\s*$|$)""",
                """\|url=(?:|(\w+:\/+)?[^|\/:]+(:\d+)?({uri_path}\/[^?"|]+)[^|]*)(\||\"|\s*$|$)""",
                """\|url=(?:|(\w+:\/+)?[^|\/:]+(:\d+)?[^|?]+({uri_query}\?.+?))(\|\w+=|\"|\s*$|$)""",
                """\|urlCategories=(?:|({event_category}[^,|]+))(,|\|)""",
                """\|(?:recv|BtS|dstBytes)=({bytes_in}\d+)""",
                """\|(?:sent|BfS|srcBytes)=({bytes_out}\d+)""",
                """\|blockReason=(?:|\s*({failure_reason}[^\s|][^|]+?)\s*)\|""",
        """\|blockReason=(?:|\s*({action}[^\s|][^|]+?)\s*)\|""",
                """\|blockReason=(?:|[^|]+by ({action}[^|]+))\|""",
                """\|mal=(?:|({malicious}[^|]+))\|""",
                """\|(?:mType|mime)=(?:|({mime}.+?))\s*(\||$)"""
    ]
  

}
```