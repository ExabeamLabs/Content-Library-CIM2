#### Parser Content
```Java
{
Name = "microsoft-defenderep-xml-alert-trigger-success-1009-tl"
Vendor = "Microsoft"
Product = "Microsoft Defender for Endpoint"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
Conditions = [
"""<eventid>1009</eventid>"""
"""<channel>microsoft-windows-windows defender/operational</channel>"""
"""<data name='product name'>microsoft defender antivirus</data>"""
]
Fields = [
"""(?i)<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)'\/>"""
"""(?i)<Computer>({host}[^<]+)<\/Computer>"""
"""(?i)<EventID>({event_code}\d+)<\/EventID>"""
"""(?i)<Security UserID='({user_sid}[^'>]+)'\/>"""
"""(?i)<Data Name ='Domain'>({domain}[^<]+)<\/Data>"""
"""(?i)<Data Name ='User'>({user}[^<]+)<\/Data>"""
"""(?i)<Data Name ='Detection User'>(({domain}[^\<]+)\\)?({user}[^<]+)<\/Data>"""
"""(?i)<Data Name ='Severity ID'>({alert_severity}\d+)<\/Data>"""
"""(?i)<Data Name ='Severity Name'>({alert_severity}[^<]+)<\/Data>"""
"""(?i)<Data Name ='Type Name'>({alert_type}[^<]+)<\/Data>"""
"""(?i)<Data Name ='Threat Name'>({alert_name}[^<]+)<\/Data>"""
"""(?i)<Data Name ='Threat ID'>({threat_id}\d+)<\/Data>"""
]
ParserVersion = "v1.0.0"


}
```