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
    """\sserverip=(?:0.0.0.0|({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))""",
    """\suseragent=({user_agent}.+?)\s+(\w+=|$)""",
    """\sClientIP=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
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