#### Parser Content
```Java
{
Name = cisco-netsec-str-network-notification-success-ftd
  Vendor = Cisco
  Product = Cisco Network Security
  ParserVersion = v1.0.0
  TimeFormat = ["MMM dd yyyy HH:mm:ss","MMM dd HH:mm:ss"]
  Conditions = [ """%FTD-""" ]
  Fields = [
  	"""({time}\w+\s+\d+(\s+\d+)?\s\d\d:\d\d:\d\d)\s(({host}[\w\-\.]+)\s):\s*(%FTD\-|\w+\s)""",
  	"""%FTD\-({priority}\d+)\-({event_code}\d+):""",
  	"""%FTD\-\d+\-\d+:\s*({additional_info}[^$]+)\s*$""",
   	"""\sfrom\s*(\w+)?(:|\s)({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\/({src_port}\d+))?\s*to\s*(\w+)?(:|\s)({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\/({dest_port}\d+))?""",
  	"""({protocol}ICMP|TCP|UDP)"""
    """\sGroup\s*<({group_name}[^>]+)>"""
    """\sUser\s*<({user}[\w\.\-\!\#\^\~]{1,40}\$?)>"""
    """packet\s+(-|({bytes}\d+))\s+"""
    """IP (=\s|<)({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?>"""
    """(src(_addr)?|Local)\s*(:|=)\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))((:|\/)({src_port}\d+))?(,|\s)"""
    """(dest_(addr)|Remote)?\s*(:|=)\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))((:|\/)({dest_port}\d+))?,"""
    """label length ({bytes}\d+) """
    """%FTD-\d+-\d+.*?({result}(?i)dropped|drop|Deny|failure|failed|fail|rejected|denied|reject|bad)"""
  ]


}
```