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
         """Text:\s*\[({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
         """Key:\s*({email_address}({user}[^"@\\\/\s,]+)(@({email_domain}[^,]+))?)""",
     
}
```