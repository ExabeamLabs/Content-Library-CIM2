#### Parser Content
```Java
{
Name = onapsis-o-cef-alert-trigger-success-osp
  Product = Onapsis
  Conditions = [ """CEF:""", """|Onapsis|OSP|""", """OnapsisOSPPolicy=""" ]
  Fields = ${OnapsisParsersTemplates.cef-onapsis-activity.Fields}[
    """\Wcat=(None|({alert_type}.+?))(\s+\w+=|\s*$)""",
    """\Wsev=({alert_severity}\d+)""",
    """\Wmsg=(None|({alert_name}.+?))(\s+\w+=|\s*$)""",
  ]
  ParserVersion = "v1.0.0"

cef-onapsis-activity = {
    Vendor = Onapsis
    TimeFormat = "MMM dd yyyy HH:mm:ss"
    Fields = [
      """CEF:([^\|]*\|){5}\s*({event_name}[^\|]+?)\s*\|""",
      """\Wend=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
      """\Wcat=(None|({category}.+?))(\s+\w+=|\s*$)""",
      """\Wdhost=(__EMPTY__|({dest_host}.+?))(\s+\w+=|\s*$)""",
      """\Wdpt=({dest_port}\d+)""",
      """\Wspt=({src_port}\d+)""",
      """\Wdst=({dest_ip}[a-fA-F\d.:]+)""",
      """\Wproto=(None|({protocol}.+?))(\s+\w+=|\s*$)""",
      """\Wreason=(None|({failure_reason}.+?))(\s+\w+=|\s*$)""",
      """\WrequestClientApplication=(None|({app}.+?))(\s+\w+=|\s*$)""",
      """\Wshost=(None|({src_host}.+?))(\s+\w+=|\s*$)""",
      """\Wsuser=(None|({user}.+?))(\s*TAG:|\s+\w+=|\s*$)""",
      """\WTAG:\s*({tag}.+?)(\s*\w+=|\s*$)""",
    
}
```