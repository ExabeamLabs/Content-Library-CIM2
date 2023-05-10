#### Parser Content
```Java
{
Name = microsoft-defenderep-xml-alert-trigger-success-1009
  Vendor = Microsoft
  Product = Microsoft Defender for Endpoint
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<EventID>1009</EventID>""", """<Channel>Microsoft-Windows-Windows Defender/Operational</Channel>""", """<Data Name ='Product Name'>Microsoft Defender Antivirus</Data>""" ]
  Fields = [
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)'\/>""",
    """<Computer>({host}[^<]+)<\/Computer>""",
    """<EventID>({event_code}\d+)<\/EventID>""",
    """<Security UserID='({user_sid}[^'>]+)'\/>""",
    """<Data Name ='Domain'>({domain}[^<]+)<\/Data>""",
    """<Data Name ='User'>({user}[^<]+)<\/Data>""",
    """<Data Name ='Detection User'>(({domain}[^\<]+)\\)?({user}[^<]+)<\/Data>""",
    """<Data Name ='Severity ID'>({alert_severity}\d+)<\/Data>""",
    """<Data Name ='Severity Name'>({alert_severity}[^<]+)<\/Data>""",
    """<Data Name ='Type Name'>({alert_type}[^<]+)<\/Data>""",
    """<Data Name ='Threat Name'>({alert_name}[^<]+)<\/Data>""",
    """<Data Name ='Threat ID'>({threat_id}\d+)<\/Data>"""
  ]
  ParserVersion = "v1.0.0"


}
```