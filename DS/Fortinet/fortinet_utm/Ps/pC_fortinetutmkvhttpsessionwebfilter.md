#### Parser Content
```Java
{
Name = fortinet-utm-kv-http-session-webfilter
  ParserVersion = v1.0.0
  Vendor = Fortinet
  Product = Fortinet UTM
  TimeFormat = "yyyy-MM-dd' time='HH:mm:ss"
  Conditions = [ 
"""subtype="""
"""webfilter"""
"""devname="""
"""date="""
"""url="""
]
  Fields = [
    """\Wdate=({time}\d\d\d\d-\d\d-\d\d time\=\d\d:\d\d:\d\d([+-]\d\d:\d\d)?)""",
    """\Wdevname="*({host}[^\s"]+)"*(\s|")""",
    """\Waction="*({action}[^\s"]+)"*(\s|")""",
    """\Wstatus="*({action}[^"]+)"""",
    """\Wurl="*(?:-|\w+:\/+[^\/]+)?({uri_path}\/[^?\s"]*)""",
    """\Wurl="*(?:[^?]+?(|({uri_query}\?[^\s"]+)))["\s]*(\w+=|$)""",
    """\Wcatdesc="*(\.+|({category}[^"]+?))["\s]*(\w+=|$|,)""",
    """\Wuser="*({user}[^"\s]+)""",
    """\Wsrcip=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wdstip=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Whostname="*({web_domain}[^"\s]+)""",
    """\Wservice="*({protocol}[^\s"]+)"*(\s|")""",
    """\Wlevel="*({alert_severity}[^\s"]+)"*(\s|")""",
    """\Wdstport=({dest_port}\d+)(\s|")""",
    """\Wsentbyte=({bytes_out}\d+)(\s|")""",
    """\Wrcvdbyte=({bytes_in}\d+)(\s|")""",
    """\Wdevid="*({host_id}[^"\s]+)"*(\s|")""",
    """\Wreferralurl="*(\.+|({referrer}[^"\s]+))""",
    """\Wgroup="*({user_group_name}[^=]+?)["\s]*(\w+=|$)""",
    """\Wmsg="*({additional_info}[^=]+?)["\s]*(\w+=|$)""",
    """\Waction="*blocked"*[^=]+?\Wmsg="*({failure_reason}[^=]+?)["\s]*(\w+=|$)""",
    """\Wmsg="*({failure_reason}[^=]+?)["\s]*(\w+=|$)[^=]+?\Waction="*blocked"*""",
    """\Wurl="({url}[^"]+)"""",
    """policyid=({policy_id}\d+)"""
  ]


}
```