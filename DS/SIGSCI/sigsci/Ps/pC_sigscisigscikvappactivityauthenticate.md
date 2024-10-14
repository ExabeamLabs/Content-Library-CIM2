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
    """Subject:\s*Security ID:\s*(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\/*({domain}[^\s]+)?""",
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