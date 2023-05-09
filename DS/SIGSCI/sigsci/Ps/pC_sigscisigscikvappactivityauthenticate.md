#### Parser Content
```Java
{
Name = sigsci-sigsci-kv-app-activity-authenticate
  Vendor = SIGSCI
  Product = SIGSCI
  TimeFormat ="yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [
    """EAP Reason Code:""",
    """Interface GUID:""",
    """Peer MAC Address:"""
  ]
  Fields = [
    """Subject:\s*Security ID:\s*({user}[^\s\/]+)\/*({domain}[^\s]+)?""",
    """Account Name:\s*\s*(-|({account_name}[^\s]+))""",
    """Account Domain:\s*\s*(-|({account_domain}[^\s]+))""",
    """Logon ID:\s*\s*({login_id}[^\s]+)""",
    """Network Information:\s*Name\s*\(SSID\):\s*({ssid}[^\s]+)""",
# interface_guid is removed
    """Local MAC Address:\s*({src_mac}[^\s]+)""",
# peer_mac_address is removed
    """Additional Information:\s*Reason Code:\s*({result_reason}.+?)\s*Error Code:"""
  ]
  ParserVersion = "v1.0.0"


}
```