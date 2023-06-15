#### Parser Content
```Java
{
Name = zscaler-ia-kv-alert-trigger-success-alerttrigeerd
  Vendor = Zscaler
  Product = Zscaler Internet Access
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """dlpengine=""", """dlpdictionaries=""", """event_id=""", """url=""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s""",
    """\saction=({result}[^=]+?)\s+\w+=""",
    """\sprotocol=({protocol}[^\s]+)\s+\w+=""",
    """\sClientIP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sserverip=(?:0.0.0.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """\suseragent=({user_agent}[^=]+?)\s+\w+=""",
    """\suser=(({email_address}[^\s@]+@[^\s\.]+\.[^\s=]+?)|({user}[^\s@=]+?))\s+\w+=""",
    """\shostname=({host}[\w\-.]+)\s+(\w+=|$)""",
    """\sdlpengine=({alert_name}[^=]+?)\s+(\w+=|$)""",
    """\surl=({target}[^\s]+)\s+(\w+=|$)""",
    """responsesize=({bytes_in}\d+)""",
    """requestsize=({bytes_out}\d+)""",
    """requestmethod=({method}[^\s]+)""",
    """\sodevicehostname=({src_host}[^\s]+)""",
    """\sodeviceowner=(NA|({device_owner}[^\s]+))"""
  ]


}
```