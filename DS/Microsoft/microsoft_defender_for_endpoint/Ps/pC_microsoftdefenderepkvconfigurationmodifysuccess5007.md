#### Parser Content
```Java
{
Name = microsoft-defenderep-kv-configuration-modify-success-5007
 Vendor = Microsoft
 ParserVersion = "v1.0.0"
 Product = "Microsoft Defender for Endpoint"
 TimeFormat = "yyyy-MM-dd HH:mm:ss"
 Conditions = [ """EventCode=5007""", """LogName =Microsoft-Windows-Windows Defender/Operational""", """SourceName =Microsoft-Windows-Windows Defender""" ]
 Fields = [
   """ComputerName =({host}[^\s]+)""",
   """EventCode=({event_code}\d+)""",
   """Sid=({user_sid}[^\s]+)""",
   """Message=({additional_info}[^\.]+)\."""
 ]
 DupFields = [ "additional_info->event_name" ]


}
```