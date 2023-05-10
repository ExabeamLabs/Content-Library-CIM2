#### Parser Content
```Java
{
Name = fortinet-utm-kv-http-session-appctrl
  ParserVersion = v1.0.0
  Vendor = Fortinet
  Product = Fortinet UTM
  TimeFormat = "yyyy-MM-dd' time='HH:mm:ss"
  Conditions = [ """subtype=""","""app-ctrl""", """eventtype=""","""app-ctrl-all""", """date=""" ]
  Fields = [
    """\Wdate=({time}\d\d\d\d-\d\d-\d\d time\=\d\d:\d\d:\d\d)"""
    """\Wdevname="*({host}[\w.-]+)""""
    """\Wsubtype="*({event_subtype}[^\"]+?)\"*(\s+\w+=|\s*$)"""
    """\Wuser="({user}[^\"]+?)""""
    """\Wsrcip=({src_ip}[a-fA-F\d.:]+)\s"""
    """\Wdstip=({dest_ip}[a-fA-F\d.:]+)\s"""
    """\Wapp="({app}[^\"]+)""""
    """\Waction="*({operation}[^\"]+?)"*(\s+\w+=|\s*$)"""
    """\Wmsg="({additional_info}[^\"]+)""""
    """\Wauthserver="({auth_server}[^\"]+)""""
    """\Wsrcport=({src_port}\d+)"""
    """\Wdstport=({dest_port}\d+)"""
    """\Whostname="({web_domain}[^\"]+)""""
    """\Wservice="({protocol}[^\"]+)""""
    """\Wurl="({uri_path}[^\"]+)""""
    """\Wappcat="({category}[^\"]+)""""
    """\Wsubtype="({event_name}[^\"]+)""""
   ]
  DupFields = [
    "operation->action"
   ]


}
```