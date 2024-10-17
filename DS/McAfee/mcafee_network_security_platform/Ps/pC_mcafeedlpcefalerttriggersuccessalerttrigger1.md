#### Parser Content
```Java
{
Name = mcafee-dlp-cef-alert-trigger-success-alerttrigger-1
  ParserVersion = v1.0.0
  Vendor = McAfee
  Product = McAfee Network Security Platform
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|McAfee|IntruShield|""" ]
  Fields = [
    """\WeventId=(|({alert_id}.+?))(\s+\w+=|\s*$)""",
    """\WcategoryOutcome=(|\/({action}.+?))(\s+\w+=|\s*$)""",
    """\WcategoryObject=(|({target}.+?))(\s+\w+=|\s*$)""",
    """\Wseverity=({alert_severity}\d+)""",
    """\Wact=(|({result}.+?))(\s+\w+=|\s*$)""",
    """\Wrt=({time}\d{13})(\s+\w+=|\s*$)""",
    """\Wsuid=(\d+|(({domain}[^\\\/=]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)""",
    """\Wsntdom=(|({domain}.+?))(\s+\w+=|\s*$)""",
    """\Wrequest=(|({url}.+?))(\s+\w+=|\s*$)""",
    """\Wdvc=(|({host}.+?))(\s+\w+=|\s*$)""",
    """\Wdvchost=(|({host}.+?))(\s+\w+=|\s*$)""",
    """\|McAfee\|IntruShield\|([^|]+?\|){2}({alert_name}[^|]+)\|""",
    """\Wcatdt=(|({alert_type}.+?))(\s+\w+=|\s*$)"""
  ]


}
```