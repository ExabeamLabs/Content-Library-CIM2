#### Parser Content
```Java
{
Name = mcafee-dlp-cef-alert-trigger-success-alerttrigger
  ParserVersion = v1.0.0
  Vendor = McAfee
  Product = McAfee SiteAdvisor
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|McAfee|SiteAdvisor Enterprise|""" ]
  Fields = [
    """\WeventId=(|({alert_id}.+?))(\s+\w+=|\s*$)""",
    """\WcategoryOutcome=(|\/({action}.+?))(\s+\w+=|\s*$)""",
    """\WcategoryObject=(|({target}.+?))(\s+\w+=|\s*$)""",
    """\Wseverity=({alert_severity}\d+)""",
    """\Wact=(|({result}.+?))(\s+\w+=|\s*$)""",
    """\Wrt=({time}\d{13})(\s+\w+=|\s*$)""",
    """\Wsuid=(|(({domain}[^\\\/=]+?)[\\\/]+)?({user}[\w\.\-]{1,40}\$?))(\s+\w+=|\s*$)""",
    """\Wsntdom=(|({domain}.+?))(\s+\w+=|\s*$)""",
    """\Wrequest=(|({malware_url}.+?))(\s+\w+=|\s*$)""",
    """\Wdvc=(|({host}.+?))(\s+\w+=|\s*$)""",
    """\Wdvchost=(|({host}.+?))(\s+\w+=|\s*$)""",
    """\Wcatdt=(|({alert_type}.+?))(\s+\w+=|\s*$)"""
    """\WrequestProtocol=(|({protocol}.+?))\s\w+=""",
  ]
  DupFields = ["alert_type->alert_name"]


}
```