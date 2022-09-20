#### Parser Content
```Java
{
Name = mcafee-dlp-kv-printer-activity-success-printing
  Vendor = McAfee
  Product = McAfee DLP
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """IncidentType="""", """ViolationLocalTime="""", """RulesToDisplay=""", """Printing""", """FileName =""" ]
  Fields = [
     """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d{1,100}), IncidentId""",
     """\sApplicationProductName ="*({app}[^"]+)""",
     """\sTotalContentSize="*({bytes}\d+)""",
     """\sIP="*({dest_ip}[a-fA-F:\d.]+)""",
     """\sRulesToDisplay="*({event_name}[^"]+)""",
     """\sName ="*({host}[^"]+)""",
     """\sFileName ="*({object}[^"]+)""",
     """\sdestination="*({printer_name}[^"]+)""",
     """\sUsername_NTLM="*(({domain}[^\\]+)\\*)?({user}[^"]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```