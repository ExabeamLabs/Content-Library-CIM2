#### Parser Content
```Java
{
Name = microsoft-defenderep-xml-report-create-success-1151
  ParserVersion = "v1.0.0"
  Product = "Microsoft Defender for Endpoint"
  Conditions = [ """<EventID>1151</EventID>""", """Microsoft-Windows-Windows Defender/Operational""" ]

xml-windows-defender-av = {
   Vendor = Microsoft
   TimeFormat = "yyyy-MM-dd HH:mm:ss"
   Fields = [
     """<EventID>({event_code}\d+)""",
     """<Computer>({host}[^<]+)""",
     """UserID\\*='({user_sid}[^']+)'""",
     """<Keywords>({result}[^<]+)<""",
     """Guid\\*='\{({provider_guid}[^}']+)"""
  
}
```