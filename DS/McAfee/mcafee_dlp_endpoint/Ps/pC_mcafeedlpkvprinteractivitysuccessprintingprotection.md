#### Parser Content
```Java
{
Name = mcafee-dlp-kv-printer-activity-success-printingprotection
  Vendor = McAfee
  Product = McAfee DLP Endpoint
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """OUTGOING_PRINTER""", """DLP: Printing Protection""" ]
  Fields = [
     """UserName ="({domain}[^\\]+)\\({user}[\w\.\-]{1,40}\$?)"""",
     """ComputerName ="({src_host}[^"]+)"""",
     """FocusDisplay="({printer_name}[^"]+)"""",
     """XmlEvidence.+?FILE_NAME.+?>({object}[^<]+)<""",
     """XmlEvidence.+?FILE_NAME.+?size="({bytes}\d+)""",
     """({operation}Printing)""",
     """ProcessInfo_FileName ="({process_name}[^"]+)""",
     """ReactionSet_DisplayName ="({result}[^"]+)""",
     """RuleIDSet_DisplayName ="({additional_info}[^"]+)""",
     """UTCTime="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
  ]
  ParserVersion = "v1.0.0"


}
```