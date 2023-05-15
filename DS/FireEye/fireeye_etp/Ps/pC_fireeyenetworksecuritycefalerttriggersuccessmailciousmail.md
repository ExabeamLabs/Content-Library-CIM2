#### Parser Content
```Java
{
Name = fireeye-networksecurity-cef-alert-trigger-success-mailciousmail
  Vendor = FireEye
  Product = FireEye ETP
  TimeFormat = "MMM dd yyyy HH:mm:ss z"
  Conditions = [ """CEF:""", """|FireEye|ETP|""", """suser=""", """mailcious email""" ]
  Fields = [
    """\|FireEye\|([^|]*\|){3}({alert_type}[^|]+)""",
    """\|FireEye\|([^|]*\|){4}({alert_severity}[^|]+)""",
    """\Wrt=({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d \w+)""",
    """\Wfname=({additional_info}[^=]+?)(\s+\w+=|\s*$)""",
    """\WdestinationDnsDomain=({domain}[^=]+?)(\s+\w+=|\s*$)""",
    """\Wsuser=({src_user}[^@\s]+)""",
    """\Wduser=({dest_user}[^@\s]+)""",
    """\Wduser=({email_address}[^@\s,]+@[^@\s,]+)""",
    """\Wduser=({user}[^@\s,]+)""",
    """\Wcs1=({alert_name}[^=]+?)(\s+\w+=|\s*$)""",
    """\Wact=({action}[^=]+?)(\s+\w+=|\s*$)""",
    """\Wcs3=({email_subject}[^=]+?)(\s+\w+=|\s*$)"""
  ]
  ParserVersion = "v1.0.0"


}
```