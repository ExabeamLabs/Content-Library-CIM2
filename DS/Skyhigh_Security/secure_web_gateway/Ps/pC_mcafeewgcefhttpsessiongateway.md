#### Parser Content
```Java
{
Name = mcafee-wg-cef-http-session-gateway
  ParserVersion = v1.0.0
  Vendor = Skyhigh Security
  Product = Secure Web Gateway
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ 
    """CEF:""",
    """|McAfee|Web""" ,"""Gateway|"""
  ]
  Fields = [
    """\Wrt=({time}\w{1,3} \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
    """\Wrt=({time}\d{13})""",
    """act=({action}\S+)""",
    """\Wcs4=({category}[^=]+)\s\w+=""",
    """\WcategoryOutcome=\/?({action}[^\/]+?)\s*([\w\.]+=|$)""",
    """\Wdvc=({host}[^=]+?)\s*([\w\.]+=|$)""",
    """\Wapp=({protocol}[^=]+?)\s*([\w\.]+=|$)""",
    """\Wsuser=(-|\([^\)]+\)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*([\w\.]+=|$)""",
    """\WfileType=({mime}[^=]+?)(\s+[\w\.]+=|\s*$)""",
    """\WrequestMethod=({method}[^=]+?)(\s+[\w\.]+=|\s*$)""",
    """\Wrequest=({url}(?:\w+:\/\/)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({web_domain}[a-zA-z0-9.\-_]+(\.[a-zA-Z]{2,})?)?)(:({dest_port}\d+))?({uri_path}\/.*?)?)(\s+[\w\.]+=|\s*$)""",
    """\WrequestClientApplication=({user_agent}[^=]+?)\s*([\w\.]+=|$)""",
    """\Wreason=({failure_reason}[^=]+?)\s*([\w\.]+=|$)""",
    """\Wrequest=({url}[^\s=]+?({uri_path}\/[^?\s]+?)?({uri_query}\?[^\s"]+)?)(\s+[\w\.]+=|\s*$)""",
    """\WflexNumber1=({dest_port}\d+)\s+(flexNumber1Label=Port|[\w\.]+=.+?flexNumber1Label=Port)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Win=({bytes_out}\d+)""",
    """\Wout=({bytes_in}\d+)""",
    """\Wcs6=({categories}(({category}[^,=]+))?(\s*,[^=]*?)?)\s+(?:cs6Label=Categories|[\w\.]+=.+?cs6Label=Categories)""",
    """\Wcs5=({action}[^=]+?)\s+(?:cs5Label=Block Reason|[\w\.]+=.+?cs5Label=Block Reason)""",
    """\|McAfee\|Web\s*Gateway\|[^\|]*\|({http_response_code}\d+)"""
  ]


}
```