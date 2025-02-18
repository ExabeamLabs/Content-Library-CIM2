#### Parser Content
```Java
{
Name = microsoft-defenderep-kv-alert-trigger-success-1116-1
 Vendor = Microsoft
 Product = Microsoft Defender
 ParserVersion = "v1.0.0"
 TimeFormat = "yyyy-MM-dd HH:mm:ss"
 Conditions = [ """EventCode=1116""", """LogName =Microsoft-Windows-Windows Defender/Operational""", """Detection Origin:""", """Detection Type:""", """Detection Source:""", """Signature Version:""" ]
 Fields = [
   """ComputerName =({host}[^\s]+)""",
   """EventCode=({event_code}\d+)""",
   """User:\s*(NT AUTHORITY|({domain}[^\\]+))(\\)?(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
   """Sid=({user_sid}[^\s]+)""",
   """Message=({additional_info}[^\.]+)\.""",
   """Name:\s*({alert_name}[^\s]+)""",
   """Detection Type:\s*({alert_type}[^\s]+)""",
   """Severity:\s*({alert_severity}[^\s]+)"""
 ]


}
```