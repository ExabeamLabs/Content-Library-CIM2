#### Parser Content
```Java
{
Name = hp-arubaos-str-endpoint-login-success-5209
 ParserVersion = "v1.0.0"
 Vendor = HP
 Product = ArubaOS
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
 Conditions = [ """5209""", """User """, """ logged in from """, """ through SSH session""" ]
 Fields = [ 
   """User\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+logged"""
   """({event_code}5209)"""
   """({protocol}SSH)"""
   """({event_name}User \S+ logged in)"""
   """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d)\s+({host}[\w\-\.]+)"""
   """logged in from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
 ]


}
```