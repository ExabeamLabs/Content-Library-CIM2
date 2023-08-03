#### Parser Content
```Java
{
Name = ibm-racf-cef-app-login-ibmracf
  ParserVersion = v1.0.0
  Vendor = IBM
  Product = IBM Resource Access Control Facility
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|IBM|Racf|""" ]
  Fields = [
    """CEF:([^\|]*\|){4}({event_code}[^\|]+)\|({operation}[^\|]+)""",
    """\Wrt=({time}\d{13})""",
    """\Wdvc=(|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}.+?))(\s+\w+=|\s*$)""",
    """\WcategoryOutcome=(|/({result}.+?))(\s+\w+=|\s*$)""",
    """\Wshost=(|({src_host}.+?))(\s+\w+=|\s*$)""",
    """\Wdhost=(|({host}.+?))(\s+\w+=|\s*$)""",
    """\Wsuser=(|({user}[\w\.\-]{1,40}\$?))(\s+\w+=|\s*$)""",
    """\Wsuid=(|({user_id}.+?))(\s+\w+=|\s*$)""",
    """\Wsproc=(Null|({process_name}.+?))(\s+\w+=|\s*$)""",
    """\Wfname=(|({object}.+?))(\s+\w+=|\s*$)""",
    """\Wcs1=(|({group_name}.+?))(\s+\w+=|\s*$)""",
    """\Wcs2=(Null|({terminal}.+?))(\s+\w+=|\s*$)""",
    """\Wcs3=(|({operation}.+?))(\s+\w+=|\s*$)""",
    """\Wcs4=(|(({src_domain}[^\\\/=]+)[\\\/]+)?({src_user}[^\\\/=]+?))(\s+\w+=|\s*$)""",
    """\Wcs5=(|({environment}.+?))(\s+\w+=|\s*$)""",
    """\Wcs6=(NONE|({additional_info}.+?))(\s+\w+=|\s*$)""",
    """\WflexString1=(|({manager_name}.+?))(\s+\w+=|\s*$)""",
    """\WflexString2=(|({manager}.+?))(\s+\w+=|\s*$)""",
    """\WflexString1Label=(|({identifier}.+?))(\s+\w+=|\s*$)""",
    """\Wcs6Label=(|({alert_type}.+?))(\s+\w+=|\s*$)""",
  ]
  DupFields = [ "terminal->app" ]


}
```