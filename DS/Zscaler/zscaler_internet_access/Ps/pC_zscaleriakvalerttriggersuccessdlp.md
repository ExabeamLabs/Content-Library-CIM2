#### Parser Content
```Java
{
Name = zscaler-ia-kv-alert-trigger-success-dlp
  Vendor = Zscaler
  Product = Zscaler Internet Access
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """dlpengine=""", """vendor=Zscaler""", """event_id=""", """url=""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d+:\d+:\d+)""",
    """\saction=({action}.+?)\s+(\w+=|$)""",
    """\sprotocol=({protocol}.+?)\s+(\w+=|$)""",
    """\sserverip=(?:0.0.0.0|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """\suseragent=({user_agent}.+?)\s+(\w+=|$)""",
    """\sClientIP=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\suser=({domain}[\w.\-]+)->({user}.+?)(\s+\w+=|\s+$)""",
    """\suser=(?![^\s]+@[^\s]+)({user}[^\s]+)\s+(\w+=|$)""",
    """\suser=(?=[^\s]+@[^\s]+)({email_address}({user}[^\s@]+)@[^\s]+)\s+(\w+=|$)""",
    """\shostname=({host}[\w\-.]+)\s+(\w+=|$)""",
    """\sdlpengine=({alert_name}.+?)\s+(\w+=|$)""",
    """\sprotocol=({alert_type}.+?)\s+(\w+=|$)""",
    """\surl=({target}.+?)\s+(\w+=|$)""",
  ]
  DupFields = [ "user_agent->browser" ]


}
```