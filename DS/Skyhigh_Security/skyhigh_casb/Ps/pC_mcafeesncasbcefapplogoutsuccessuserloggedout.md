#### Parser Content
```Java
{
Name = mcafee-sncasb-cef-app-logout-success-userloggedout
    Vendor = Skyhigh Security
    Product = Skyhigh CASB
    ParserVersion = "v1.0.0"
    TimeFormat = "MMM dd yyyy HH:mm:ss.SSS z"
    Conditions = [ """|McAfee (Skyhigh)|Dashboard Audit Logs|""", """User logged out""" ]
    Fields = [
      """\Wcat=(|({alert_type}.+?))(\s+\w+=|\s*$)""",
      """({host}[\w.\-]+)\s+(LEEF|CEF):""",
      """CEF:([^\|]+\|){5}({operation}[^\|\s]+)\|""",
      """\W(start|devTime)=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d\.\d+ \w+)""",
      """\WobjectName =(|({object}.+?))(\s+\w+=|\s*$)""",
      """\WuserInfoEmail=(|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))(\s+\w+=|\s*$)""",
      """\WuserInfoFirstName =(|({first_name}.+?))(\s+\w+=|\s*$)""",
      """\WuserInfoLastName =(|({last_name}.+?))(\s+\w+=|\s*$)""",
    ]
  

}
```