#### Parser Content
```Java
{
Name = checkpoint-tp-cef-alert-trigger-success-checkpointsmartdefense
  Vendor = Check Point
  Product = Threat Prevention
  ParserVersion = v1.0.0
  TimeFormat = "epoch"
  Conditions = [ """|Check Point|SmartDefense""", """cp_severity=""" ]
  Fields = [
    """({host}[\w.\-]+) CEF:""",
    """\Wcp_severity=(?:|({alert_severity}.+?))(\s+\w+=|\s*$)""",
    """\Wrt=({time}\d+)""",
    """\Wsrc=({src_ip}[a-fA-F\d.:]+)""",
    """\Wdst=({dest_ip}[a-fA-F\d.:]+)""",
    """\Woriginsicname=(?:|({user_ou}.+?))(\s+\w+=|\s*$)""",
    """\Wmsg=(?:|({alert_type}.+?))(\s+\w+=|\s*$)""",
    """\Wdescription_url=(?:|({malware_url}.+?))(\s+\w+=|\s*$)""",
    """\Wcs4=(?:|({alert_name}.+?))(\s+\w+=|\s*$)""",
    """\Winspection_information=(?:|({alert_name}.+?))(\s+\w+=|\s*$)""",
    """\WflexString2=(?:|({additional_info}.+?))(\s+\w+=|\s*$)""",
    """\Wproto=(?:|({protocol}.+?))(\s+\w+=|\s*$)""",
    """\Wspt=({src_port}\d+)""",
    """\Wdpt=({dest_port}\d+)""",
  ]


}
```