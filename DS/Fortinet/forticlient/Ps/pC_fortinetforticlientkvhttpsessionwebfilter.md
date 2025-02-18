#### Parser Content
```Java
{
Name = fortinet-forticlient-kv-http-session-webfilter
  ParserVersion = v1.0.0
  Vendor = Fortinet
  Product = FortiClient
  TimeFormat = ["yyyy-MM-dd' time='HH:mm:ss","yyyy-MM-dd 'time='HH:mm:ssz"]
  Conditions = [ 
"""subtype="webfilter""""
"""devname=""""
""" devid="""
"""msg=""""
"""status=""""
]
  Fields = [
    """date=({time}\d\d\d\d-\d\d-\d\d time\=\d\d:\d\d:\d\d([+-]\d\d:\d\d)?)""",
    """\Wdevname="*({host}[^\s"]+)"*(\s|")""",
    """\Wstatus="*({action}[^"]+)"""",
    """\Waction="*({action}[^\s"]+)"*(\s|")""",
    """\suser="*(({email_address}[^@"\s]+@[^\."\s]+\.[^"\s]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^"\s]+))?)("|\s)""",
    """\Wip="*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Whostname="*({web_domain}[^"\s]+)""",
    """\Wservice="*({protocol}[^\s"]+)"*(\s|")""",
    """\Wlevel="*({severity}[^\s"]+)"*(\s|")""",
    """\Wdevid="*({asset_id}[^"\s]+)"*(\s|")""",
    """\Wmsg="*({additional_info}[^=]+?)["\s]*(\w+=|$)""",
    """\Waction="*blocked"*[^=]+?\Wmsg="*({result_reason}[^=]+?)["\s]*(\w+=|$)""",
    """\Wmsg="*({result_reason}[^=]+?)["\s]*(\w+=|$)[^=]+?\Waction="*blocked"*""",
    """\Wtz="?({tz}[+-]\d+)"""
  ]


}
```