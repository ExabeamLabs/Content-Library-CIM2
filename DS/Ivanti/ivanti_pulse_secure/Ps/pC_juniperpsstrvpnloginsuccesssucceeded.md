#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-login-success-succeeded
    ParserVersion = v1.0.0
    Vendor = Ivanti
    Product = Ivanti Pulse Secure
    TimeFormat = ["yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ssZ"]
    Conditions = [
""" Login succeeded for """
""" (session:"""
]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d) \- .*?Login succeeded for""",
      """(::ffff:)?({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d\d:\d\d)\s*({host}(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w.\-]+)))\s*(Juniper|PulseSecure):"""
      """PulseSecure:\s*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+({host}(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w.\-]+)))""",
      """Login succeeded for (?:({email_address}[^@\s]+@[^@\s\/]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
      """Login succeeded for [^/]+/({realm}.+?)\s+\(session:""",
      """Login succeeded for .+?from (::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """PulseSecure:.*?\[(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s+(({domain}[^\\]+)\\+)?(?:({email_address}[^@\s]+@[^@\(]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\(({realm}[^\)]+)?""",
      """Mozilla\/\d+.\d\s*\(({os}[^\)]+)\)"""
    ]
    DupFields = [ "user->account" ]
  

}
```