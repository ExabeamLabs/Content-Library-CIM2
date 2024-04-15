#### Parser Content
```Java
{
Name = "juniper-ps-str-user-delete-fail-firewall"
Vendor = "Ivanti"
Product = "Pulse Secure"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""PulseSecure:"""
"""User Accounts modified."""
"""id=firewall"""
]
Fields = [
"""time=\"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\".*vpn=({host}[^\s]+).*user=(({email_address}[^@\s\/]+@[^@\s\/]+)|({user}[^\/\s]+)).*realm=\"({realm}[^\"]+)?\".*roles=\"({role}[^\"]+)?\".*Removed username (((({dest_domain}[^\\]+)\\)?({dest_user}[^\\\s]+)))"""
]
ParserVersion = "v1.0.0"


}
```