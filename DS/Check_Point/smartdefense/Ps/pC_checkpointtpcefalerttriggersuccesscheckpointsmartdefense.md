#### Parser Content
```Java
{
Name = checkpoint-tp-cef-alert-trigger-success-checkpointsmartdefense
  Vendor = Check Point
  Product = SmartDefense
  ParserVersion = v1.0.0
  TimeFormat = "epoch"
  Conditions = [ """|Check Point|SmartDefense""", """cp_severity=""" ]
  Fields = [
    """({host}[\w.\-]+) CEF:""",
    """\Wcp_severity=(?:|({alert_severity}.+?))(\s+\w+=|\s*$)""",
    """\Wrt=({time}\d{13})""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
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