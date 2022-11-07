#### Parser Content
```Java
{
Name = ibm-datapower-str-app-notification-certificate
 Vendor = IBM
 Product = IBM Datapower
 ParserVersion = "v1.0.0"
 TimeFormat = "yyyy-MM-dd HH:mm:ss"
 Conditions = [ """[0x806000e""", """][cert-monitor]""", """] cert-monitor(Certificate Monitor): """, """: Certificate """ ]
 Fields = [
   """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+\[({event_code}[^\]\s]+)\]\[({event_category}[^\]]+)""",
   """Certificate\s+\'([^']+)\'\s+in domain\s+\'({domain}[^']+)\'""",# certificate_name is removed
   """({event_name}expired)\s+at\s+\'({expiry_time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)\'""",
   """({event_name}about to expire)\s+at\s+\'({expiry_time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)\'""",
   ]


}
```