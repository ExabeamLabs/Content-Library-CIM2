#### Parser Content
```Java
{
Name = proofpoint-tap-cef-alert-trigger-success-proofpoint
  Vendor = Proofpoint
  Product = Targeted Attack Platform
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = [ """|McAfee|ESM|""", """Proofpoint""", """nitroRule_Name =""" ]
  Fields = [
    """({host}\S+) CEF:""",
    """\Wrt=({time}\d{13})""",
    """\WnitroRule_Name =({alert_name}.+?)\s*(\w+=|$)""",
    """\WMsg_Sec_Gw\s*({event_name}[^\|]+)\|""",
    """\Wshost=({src_host}[\w\-.]+)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\WnitroCommandID=({command}.+?)\s*(\w+=|$)""",
    """\Wact=({action}.+?)\s*(\w+=|$)""",
  ]
  DupFields = [ "alert_name->alert_type" ]


}
```