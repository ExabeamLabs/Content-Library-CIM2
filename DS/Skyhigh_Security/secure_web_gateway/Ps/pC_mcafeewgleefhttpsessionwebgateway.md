#### Parser Content
```Java
{
Name = mcafee-wg-leef-http-session-webgateway
    Vendor = Skyhigh Security
    Product = Secure Web Gateway
	ParserVersion = "v1.0.0"
    TimeFormat = "epoch"
    Conditions = [ """LEEF:""","""|McAfee|Web Gateway|""" ]
    Fields = [
                """\|devTime=({time}\d{13})""",
                """\d\d:\d\d:\d\d\s({host}[^\s]+)\s(mwg:\s)?LEEF:""",
                """\|usrName =(?:|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\|""",
                """\|src=(?:|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\|""",
                """\|dst=(?:|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\|""",
                """\|httpStatus=(?:|({http_response_code}\d+))\|""",
                """\|Prot=(?:|({protocol}[^|]+))\|""",
                """\|(?:agent|usrAgent)=(?:|({user_agent}[^|]+))\|""",
                """\|Meth=(?:|({method}[^|]+))\|""",
                """\|url=(-|({url}.+?))(\|\w+=|\"|\s*$|$)""",
                """\|url=(?:|(\w+:\/+)?({web_domain}(?:({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|[^\/:|]+))[^|]*)(\||\"|\s*$|$)""",
                """\|url=(?:|(\w+:\/+)?[^|\/:]+(:\d+)?({uri_path}\/[^?"|]+)[^|]*)(\||\"|\s*$|$)""",
                """\|url=(?:|(\w+:\/+)?[^|\/:]+(:\d+)?[^|?]+({uri_query}\?.+?))(\|\w+=|\"|\s*$|$)""",
                """\|urlCategories=(?:|({category}[^,|]+))(,|\|)""",
                """\|(?:recv|BtS|dstBytes)=({bytes_in}\d+)""",
                """\|(?:sent|BfS|srcBytes)=({bytes_out}\d+)""",
                """\|blockReason=(?:|\s*({failure_reason}[^\s|][^|]+?)\s*)\|""",
        """\|blockReason=(?:|\s*({action}[^\s|][^|]+?)\s*)\|""",
                """\|blockReason=(?:|[^|]+by ({action}[^|]+))\|""",
                """\|mal=(?:|({result}[^|]+))\|""",
                """\|(?:mType|mime)=(?:|({mime}.+?))\s*(\||$)"""
    ]
  

}
```