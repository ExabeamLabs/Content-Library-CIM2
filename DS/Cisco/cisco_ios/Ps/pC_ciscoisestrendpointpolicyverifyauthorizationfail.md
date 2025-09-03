#### Parser Content
```Java
{
Name = "cisco-ise-str-endpoint-policy-verify-authorizationfail"
  Vendor = "Cisco"
  Product = "Cisco IOS"
  TimeFormat = ["MMM dd yyyy HH:mm:ss.SSS", "MMM dd HH:mm:ss"]
  Conditions = [
    """Authorization failed"""
    """%SESSION_MGR-5-FAIL:"""
   ]
  Fields = [
    """\s({time}\w+ \d+ \d+:\d+:\d+)"""
    """({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d\.\d\d\d)"""
    """({event_category}%.+?):"""
    """host\s*=\s*({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """({event_name}Authorization failed)"""
    """Authc failure reason:\s+({failure_reason}.+?)\s$"""
    """AuditSessionID\s+({session_id}[^\s]+)\."""
    """for client\s+\(({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})\)"""
    """Interface\s+({interface}[^\s]+)"""
# switch_interface is removed
    """({result}failed)"""
  ]
  ParserVersion = "v1.0.0"


}
```