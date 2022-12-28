#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-login-success-login
   ParserVersion = v1.0.0
   Vendor = Juniper Networks
   Product = Juniper Pulse Secure
   TimeFormat = "yyyy-MM-dd HH:mm:ss"
   Conditions = [ 
"""PulseSecure:"""
"""Remote address for user"""
]
   Fields = [
     """PulseSecure: (\S+\s\S+\s\S+\s)?({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d) - (::ffff:)?({host}\S+) - \[(::ffff:)?({src_ip}[A-Fa-f:\d.]+)\] (({domain}[^\\]+)\\)?({user}[^\\\/\s\(]+)""",
     """changed from (::ffff:)?({src_ip}[A-Fa-f:\d.]+) to (::ffff:)?({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
   ]
   DupFields = [ "user->account" ]
  

}
```