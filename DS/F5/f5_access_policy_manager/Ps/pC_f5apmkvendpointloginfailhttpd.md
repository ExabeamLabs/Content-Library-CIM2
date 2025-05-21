#### Parser Content
```Java
{
Name = "f5-apm-kv-endpoint-login-fail-httpd"
  ParserVersion = "v1.0.0"
  Vendor = "F5"
  Product = "F5 Access Policy Manager"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
"""pam_audit"""
""" tty="""
"""failed to login"""
]
  Fields = [
"""\w{3}\s\d\d\s\d\d:\d\d:\d\d\s([^\/\s]+\/)?({host}\S+)\sinfo"""
"""start=\"\w+\s({time_started}\w+\s*\d+\s\d\d:\d\d:\d\d\s\d\d\d\d)"""
"""end=\"\w+\s({time_ended}\w+\s*\d+\s\d\d:\d\d:\d\d\s\d\d\d\d)"""
"""host=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\sfailed"""
"""(?:u|U)ser=({domain}[^\\\s]+?\\)?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""\s({protocol}\w+)\(pam_audit\)\["""
   ]


}
```