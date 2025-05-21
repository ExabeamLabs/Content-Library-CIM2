#### Parser Content
```Java
{
Name = securelink-s-kv-app-logout-success-nexuslogout
  ParserVersion = "v1.0.0"
  Conditions = [ """ SecureLink """, """, Type: Login,""", """Nexus Logout for Vendor:""", """User:""" ]
  Fields = ${SecureLinkParsersTemplates.securelink-system-events.Fields}[
    """Nexus Logout for Vendor:\s*({app}[^\."]+)"""
  ]

securelink-system-events {
     Vendor = SecureLink
     Product = SecureLink
     TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
     Fields = [
         """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)\s+({host}[\w\-\.]+)\s"""
         """User:\s*(SYSLOG|(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-]{1,40}\$?))),""",
         """Text:\s*\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
         """Key:\s*([\d\.]+|[a-fA-F0-9]{8}-([a-fA-F0-9]{4}-){3}[a-fA-F0-9]{12}|(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)))),""",
         """Type:\s*({event_name}[^,\]]+),""",
         """Text:\s*(\[[^\]]+\]\s+)?({additional_info}[^",]+)""",
         """Method:\s*({event_category}[^,]+),"""
     
}
```