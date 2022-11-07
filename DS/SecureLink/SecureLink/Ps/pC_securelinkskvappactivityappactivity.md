#### Parser Content
```Java
{
Name = securelink-s-kv-app-activity-appactivity
  Conditions = [
    """SecureLink:""",
    """User:"""
  ]
  ParserVersion = "v1.0.0"

securelink-system-events {
     Vendor = SecureLink
     Product = SecureLink
     TimeFormat = "yyyy-MM-dd HH:mm:ss"
     Fields = [
         """User:\s*(SYSLOG|(({user}[^"@\\\/\s,]+)(@({email_domain}[^,]+))?))""",
         """Text:\s*\[({src_ip}[A-Fa-f:\d.]+)""",
         """Key:\s*({email_address}({user}[^"@\\\/\s,]+)(@({email_domain}[^,]+))?)""",
     
}
```