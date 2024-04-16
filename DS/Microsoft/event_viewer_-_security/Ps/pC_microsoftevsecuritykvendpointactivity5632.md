#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-activity-5632
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "epoch_sec"
  Conditions = [ """Microsoft-Windows-Security-Auditing""", """EventID=5632""" ]
  Fields = [
    """TimeGenerated=({time}\d{10})"""
    """EventID=({event_code}\d+)""",
    """Computer=({host}[\w\-.]+)""",
    """Keywords=({result}[^=]+?)\s+\w+=""",
    """Message=({event_name}[^:]+?)\s+\w+:""",
    """Subject:\s+Security ID:\s+(\s+|({user_sid}[^:]+?))\s+Account Name:""",
    """Subject:.+?Account Name:\s+({user}[\w\.\-]{1,40}\$?)\s+Account Domain:""",
    """Subject:.+?Account Domain:\s+({domain}[^:]+?)\s+Logon ID:""",
    """Subject:.+?Logon ID:\s+({login_id}[^\s]+)""",
    """Network Information:\s*Name\s*\(SSID\):\s*({ssid}[^\s]+)""",
    """Local MAC Address:\s*({src_mac}[^\s]+)""",
    """Additional Information:\s*Reason Code:\s*({result_reason}.+?)\s*Error Code:""",
    """Additional Information:.+?Error Code:\s+({result_code}[\w\-]+)""",
    """EAP Root Cause String:\s+(\s+|({additional_info}.+?))\s+EAP Error Code:"""
  ]
  ParserVersion = "v1.0.0"
  DupFields = [ "result_reason->failure_reason" ]


}
```