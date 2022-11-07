#### Parser Content
```Java
{
Name = securelink-s-kv-app-logout-logout
  ParserVersion = "v1.0.0"
  Conditions = [  """Logged Out.""", """SecureLink:""", """User:""" ]
  Fields = ${SecureLinkParsersTemplates.securelink-system-events.Fields}[
  """({event_name}Logged Out)"""
  ]

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