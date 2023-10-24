#### Parser Content
```Java
{
Name = mcafee-sncasb-mix-alert-trigger-success-anomalies
	ParserVersion = v1.0.0
    Vendor = McAfee
    Product = Skyhigh Networks CASB
    TimeFormat = "MMM dd yyyy HH:mm:ss.SSS z"
    Conditions = [ """|McAfee (Skyhigh)|Anomalies|""" ]
    Fields = [
      """\Wcat=(|({alert_type}.+?))(\s+\w+=|\s*$)""",
      """({host}[\w.\-]+)\s+(LEEF|CEF):""",
      """CEF:([^\|]*\|){5}({alert_type}[^\|\s]+)\|""",
      """\W(start|devTime)=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d\.\d+ \w+)""",
      """\W(suser|usrName)=(N\/A|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))""",
      """\W(riskSeverity|sev)=({alert_severity}\w+)""",
      """\WpolicyName =(null|({alert_name}.+?))(\s+\w+=|\s*$)""",
      """\W(response|status)=(|({result}.+?))(\s+\w+=|\s*$)""",
      """\WincidentId=({alert_id}\d+)""",
      """\WserviceNames=(|({additional_info}.+?))(\s+\w+=|\s*$)""",
      """\WcontentItemName =(|({malware_file_name}.+?))(\s+\w+=|\s*$)""",
      """\WtotalMatchCount=(|({total_match_count}.+?))(\s+\w+=|\s*$)"""
    ]
 

}
```