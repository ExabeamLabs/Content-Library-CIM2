#### Parser Content
```Java
{
Name = microsoft-defenderav-kv-alert-trigger-success-1116
 Vendor = Microsoft
 Product = Defender Antivirus
 ParserVersion = "v1.0.0"
 TimeFormat = "yyyy-MM-dd HH:mm:ss"
 Conditions = [ """EventCode=1116""", """LogName =Microsoft-Windows-Windows Defender/Operational""", """Detection Origin:""", """Detection Type:""", """Detection Source:""", """Signature Version:""" ]
 Fields = [
   """ComputerName =({host}[^\s]+)""",
   """EventCode=({event_code}\d+)""",
   """User:\s*(NT AUTHORITY|({domain}[^\\]+))(\\)?(SYSTEM|({user}[^\s]+))""",
   """Sid=({user_sid}[^\s]+)""",
   """Message=({additional_info}[^\.]+)\.""",
   """Name:\s*({alert_name}[^\s]+)""",
   """Detection Type:\s*({alert_type}[^\s]+)""",
   """Severity:\s*({alert_severity}[^\s]+)"""
 ]


}
```