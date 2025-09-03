#### Parser Content
```Java
{
Name = mcafee-sncasb-cef-alert-trigger-success-alertpolicy
Vendor = Skyhigh Security
Product = Skyhigh CASB
ParserVersion = "v1.0.0"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [ """CEF""", """McAfee""", """MVISION Cloud""", """|Dlp|Alert.Policy|"""]
Fields = [
"""\d\d:\d\d:\d\d\s({host}[^\s]+)\s+CEF:""",
"""riskSeverity=({alert_severity}[^\s]+)""",
"""Dlp\|({alert_type}Alert\.Policy)\|""",
"""contentItemName =({file_name}[^=]+)\s+\w+=""",
"""contentItemHierarchy=({additional_info}[^=]+)\s+\w+=""",
"""incidentId=({alert_id}[^=]+?)\s\w+=""",
"""suser=(N\/A|({email_address}[^@\s]+@({email_domain}[^\.]+\.[^\s]+)))\s+\w+=""",
"""response=\[({result}[^\]]+)\]\s+\w+=""",
"""policyName =({alert_name}[^=]+)\s+\w+=""",
"""serviceNames=\[({target}[^=]+)\]\s+\w+=""",
"""totalMatchCount=({total_match_count}\d+)\s+\w+=""",
]


}
```