#### Parser Content
```Java
{
Name = fortinet-utm-kv-http-session-appctrl
  ParserVersion = v1.0.0
  Vendor = Fortinet
  Product = Fortinet UTM
  TimeFormat = "yyyy-MM-dd' time='HH:mm:ss"
  Conditions = [ """ subtype=""","""app-ctrl""", """ eventtype=""", """date=""", """ app=""" ]
  Fields = [
    """date=({time}\d\d\d\d-\d\d-\d\d time\=\d\d:\d\d:\d\d)"""
    """\Wdevname="*({host}[\w.-]+)""""
    """\Wsubtype="*({event_subtype}[^\"]+?)\"*(\s+\w+=|\s*$)"""
    """\Wuser="({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
    """\Wsrcip="*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4}):*|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """\Wdstip="*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s"""
    """\Wapp="*({app}[^\"]+)"*(\s+\w+=|\s*$)"""
    """\Waction="*({action}[^\"]+?)"*(\s+\w+=|\s*$)"""
    """\Wmsg="({additional_info}[^\"]+)""""
    """\Wauthserver="({auth_server}[^\"]+)""""
    """\Wsrcport=({src_port}\d+)"""
    """\Wdstport=({dest_port}\d+)"""
    """\Whostname="({web_domain}[^\"]+)""""
    """\Wservice="({protocol}[^\"]+)""""
    """\Wurl="({uri_path}[^\"]+)""""
    """\Wappcat="({category}[^\"]+)""""
    """\Wsubtype="({event_name}[^\"]+)"""",
    """\Wtz="?({tz}[+-]\d+)"""
   ]


}
```