#### Parser Content
```Java
{
Name = infowatch-iw-cef-http-session-success-webmessage
  Vendor = InfoWatch
  Product = InfoWatch
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Web message|""", """|DLP|DLP TM""" ]
  Fields = [
    """\Wact=({action}.+?)(\s+[\w\.]+=|\s*$)""",
    """\Wrt=({time}\d+)""",
    """\Wsrc=({src_ip}[a-fA-F\d.:]+)""",
    """\Wsntdom=({user}[^@=]+)@({domain}[^@]+?)(\s+[\w\.]+=|\s*$)""",
    """\Wsuser=({user}.+?)(\s+[\w\.]+=|\s*$)""",
    """\Wduser=({web_domain}.+?)(\s+[\w\.]+=|\s*$)""",
    """\Wrequest=({url}(\w+:\/\/)?[^\/]+?({uri_path}\/[^\?\s]*?)({uri_query}\?.*?)?)(\s+[\w\.]+=|\s*$)""",
    """\Wdvchost=({host}.+?)(\s+[\w\.]+=|\s*$)""",
    """\Wdvc=({host}.+?)(\s+[\w\.]+=|\s*$)""",
  ]
  ParserVersion = "v1.0.0"


}
```