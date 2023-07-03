#### Parser Content
```Java
{
Name = mcafee-es-kv-file-write-success-plugandplay
  Conditions = [ """RulesToDisplay="Plug and Play""", """ViolationUTCTime=""", """Destination=""", """Username=""", """ViolationTimezone=""", """ViolationLocalTime=""" ]
  ParserVersion = "v1.0.0"
  Fields = ${McAfeeParsersTemplates.mcafee-dlp-activity.Fields} [
    """,\sDestination="*({device_type}[^"]+)"*,\s"""
  ]

mcafee-dlp-activity = {
      Vendor = McAfee
      Product = McAfee DLP Endpoint
      TimeFormat = "yyyy-MM-dd HH:mm:ss"
      Fields = [
        """,\sViolationUTCTime="*({time}\d{4}\-\d{2}\-\d{2}\s\d{2}:\d{2}:\d{2})""",
        """,\sRulesToDisplay="*({alert_name}[^"]+)"*,\s""",
        """,\sName ="*({src_host}[^"]+)"*,\s""",
        """,\sUsername="*({user}[^"]+)"*,\s""",
        """,\sFilePath="*({file_path}.+?)"*,\s""",
        """,\sFileName ="*({file_name}.+?)"*,\s""",
        """,\sFileSize="*({bytes}\d+)"*"""
        ]
    }

  cef-mcafee-skyhigh-activity = {
    Vendor = McAfee
    Product = Skyhigh Networks CASB
    TimeFormat = "MMM dd yyyy HH:mm:ss.SSS z"
    Fields = [
      """\Wcat=(|({operation}.+?))(\s+\w+=|\s*$)""",
      """({host}[\w.\-]+)\s+(LEEF|CEF):""",
      """CEF:([^\|]*\|){5}({operation}[^\|]+)""",
      """({app}Skyhigh)""",
      """\W(start|devTime)=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d\.\d+ \w+)""",
      """\W(suser|usrName)=(N\/A|({email_address}[^@=]+?@[^@=]+?)|({user}[^\s]+?))(\s+\w+=|\s*$)""",
      """\Wdescription=(|({additional_info}.+?))(\s+\w+=|\s*$)""",
      """\WobjectName =(|null|({object}.+?))(\s+\w+=|\s*$)""",
      """\WuserInfoEmail=(|({email_address}[^@]+({email_domain}.+?)))(\s+\w+=|\s*$)""",
      """\WuserInfoFirstName =(|({first_name}.+?))(\s+\w+=|\s*$)""",
      """\WuserInfoLastName =(|({last_name}.+?))(\s+\w+=|\s*$)""",
    
}
```