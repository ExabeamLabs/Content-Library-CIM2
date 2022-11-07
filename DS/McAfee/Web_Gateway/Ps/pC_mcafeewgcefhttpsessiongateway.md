#### Parser Content
```Java
{
Name = mcafee-wg-cef-http-session-gateway
  ParserVersion = v1.0.0
  Vendor = McAfee
  Product = Web Gateway
  TimeFormat = "epoch"
  Conditions = [ 
    """CEF:""",
    """|McAfee|Web Gateway|"""
  ]
  Fields = [
    """\Wrt=({time}\w{1,3} \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
    """\Wrt=({time}\d+)""",
    """\WcategoryOutcome=\/?({action}[^\/]+?)\s*([\w\.]+=|$)""",
    """\Wdvc=({host}[^=]+?)\s*([\w\.]+=|$)""",
    """\Wapp=({protocol}[^=]+?)\s*([\w\.]+=|$)""",
    """\Wsuser=(-|\([^\)]+\)|({user}[^=]+?))\s*([\w\.]+=|$)""",
    """\WfileType=({mime}[^=]+?)(\s+[\w\.]+=|\s*$)""",
    """\WrequestMethod=({method}[^=]+?)(\s+[\w\.]+=|\s*$)""",
    """\Wrequest=({url}(?:\w+:\/\/)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({web_domain}[^\/\s=]+))({uri_path}\/.*?)?)(\s+[\w\.]+=|\s*$)""",
    """\WrequestClientApplication=({user_agent}[^=]+?)\s*([\w\.]+=|$)""",
    """\Wreason=({failure_reason}[^=]+?)\s*([\w\.]+=|$)""",
    """\Wrequest=({url}[^\s=]+?({uri_path}\/[^?\s]+?)?({uri_query}\?[^\s"]+)?)(\s+[\w\.]+=|\s*$)""",
    """\WflexNumber1=({dest_port}\d+)\s+(flexNumber1Label=Port|[\w\.]+=.+?flexNumber1Label=Port)""",
    """\Wsrc=({src_ip}[A-Fa-f:\d.]+)""",
    """\Wdst=({dest_ip}[A-Fa-f:\d.]+)""",
    """\Win=({bytes_out}\d+)""",
    """\Wout=({bytes_in}\d+)""",
    """\Wcs6=({category}[^=]+?)\s+(?:cs6Label=Categories|[\w\.]+=.+?cs6Label=Categories)""",
    """\WflexString2=({category}[^=]+?)\s+(?:flexString2Label=Site Categories|[\w\.]+=.+?flexString2Label=Site Categories)""",
    """\Wcs5=({action}[^=]+?)\s+(?:cs5Label=Block Reason|[\w\.]+=.+?cs5Label=Block Reason)""",
    """\|McAfee\|Web Gateway\|[^\|]*\|({http_response_code}\d+)""",
  ]


}
```