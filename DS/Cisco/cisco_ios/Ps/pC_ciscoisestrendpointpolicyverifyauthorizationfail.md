#### Parser Content
```Java
{
Name = "cisco-ise-str-endpoint-policy-verify-authorizationfail"
  Vendor = "Cisco"
  Product = "Cisco IOS"
  TimeFormat = ["MMM dd yyyy HH:mm:ss.SSS", "MMM dd HH:mm:ss"]
  Conditions = [
    """Authorization failed"""
    """Authc failure reason:"""
   ]
  Fields = [
    """\s({time}\w+ \d+ \d+:\d+:\d+)"""
    """({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d\.\d\d\d)"""
    """({event_category}%.+?):"""
    """sessmgrd:\s+({event_name}Authorization failed)"""
    """Authc failure reason:\s+({failure_reason}.+?)\s$"""
    """AuditSessionID\s+({session_id}[^\s]+)\."""
    """for client\s+\(({src_mac}.+?)\)"""
# switch_interface is removed
    """({result}failed)"""
  ]
  ParserVersion = "v1.0.0"


}
```