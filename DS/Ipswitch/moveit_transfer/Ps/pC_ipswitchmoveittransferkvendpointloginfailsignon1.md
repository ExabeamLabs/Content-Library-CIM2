#### Parser Content
```Java
{
Name = "ipswitch-moveittransfer-kv-endpoint-login-fail-signon-1"
  ParserVersion = "v1.0.0"
  Vendor = "Ipswitch"
  Product = "MoveIt Transfer"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ 
"""MOVEitDMZ"""
"""FAILED: Sign On""" 
]
  Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""
"""\s\d\d:\d\d:\d\d\s({host}[^\s]+)"""
"""\sIPAddress:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""User\s'(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|Automation|({full_name}[^']+))?'\s\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)?\)"""
"""\s:\s+({operation}[^,]+),\s+ID:"""
"""\sUsername:\s*(Automation|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""\sMessage:\s*({failure_reason}.+?)\s*$"""
  ]


}
```