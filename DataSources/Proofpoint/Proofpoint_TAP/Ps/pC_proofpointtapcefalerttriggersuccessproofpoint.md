#### Parser Content
```Java
{
Name = proofpoint-tap-cef-alert-trigger-success-proofpoint
  Vendor = Proofpoint
  Product = Proofpoint TAP
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = [ """|McAfee|ESM|""", """Proofpoint""", """nitroRule_Name =""" ]
  Fields = [
    """({host}\S+) CEF:""",
    """\Wrt=({time}\d+)""",
    """\WnitroRule_Name =({alert_name}.+?)\s*(\w+=|$)""",
    """\WMsg_Sec_Gw\s*({event_name}[^\|]+)\|""",
    """\Wshost=({src_host}[\w\-.]+)""",
    """\Wsrc=({src_ip}[A-Fa-f:\d.]+)""",
    """\WnitroCommandID=({command}.+?)\s*(\w+=|$)""",
    """\Wact=({action}.+?)\s*(\w+=|$)""",
  ]
  DupFields = [ "alert_name->alert_type" ]


}
```