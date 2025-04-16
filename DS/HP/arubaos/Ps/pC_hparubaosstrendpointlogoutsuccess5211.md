#### Parser Content
```Java
{
Name = hp-arubaos-str-endpoint-logout-success-5211
 ParserVersion = "v1.0.0"
 Vendor = HP
 Product = ArubaOS
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
 Conditions = [ """5211""", """User """, """ logged out of SSH session from """ ]
 Fields = [ 
   """User\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+logged"""
   """({event_code}5211)"""
   """({protocol}SSH)"""
   """({event_name}User \S+ logged out)"""
   """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d)\s+({host}[\w\-\.]+)"""
   """logged out of SSH session from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
 ]


}
```