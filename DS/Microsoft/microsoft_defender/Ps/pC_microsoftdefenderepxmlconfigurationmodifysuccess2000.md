#### Parser Content
```Java
{
Name = microsoft-defenderep-xml-configuration-modify-success-2000
  ParserVersion = "v1.0.0"
  Product = "Microsoft Defender"
  Conditions = [ """<EventID>2000</EventID>""", """Microsoft-Windows-Windows Defender/Operational""" ]
  Fields = ${DLWindowsParsersTemplates.xml-windows-defender-av.Fields}[
    """<Computer>({host}[^<]+)""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  ]

xml-windows-defender-av = {
   Vendor = Microsoft
   TimeFormat = "yyyy-MM-dd HH:mm:ss"
   Fields = [
     """<EventID>({event_code}\d+)""",
     """UserID\\*='({user_sid}[^']+)'""",
     """<Keywords>({result}[^<]+)<""",
     """Guid\\*='\{({provider_guid}[^}']+)"""
     """<Level>({run_level}[^<]+)<"""
  
}
```