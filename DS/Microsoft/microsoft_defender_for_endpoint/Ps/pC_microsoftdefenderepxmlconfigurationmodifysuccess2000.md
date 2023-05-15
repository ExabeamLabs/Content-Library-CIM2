#### Parser Content
```Java
{
Name = microsoft-defenderep-xml-configuration-modify-success-2000
  ParserVersion = "v1.0.0"
  Product = "Microsoft Defender for Endpoint"
  Conditions = [ """<EventID>2000</EventID>""", """Microsoft-Windows-Windows Defender/Operational""" ]

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