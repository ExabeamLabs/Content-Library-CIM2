#### Parser Content
```Java
{
Name = "pan-gp-csv-endpoint-authentication-fail-authfail"
  Vendor = "Palo Alto Networks"
  Product = "GlobalProtect"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy/MM/dd HH:mm:ss"]
  Conditions = [
""",SYSTEM,auth,""",
""",auth-fail,"""
  ]
  Fields = [
"""\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+\d+,({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+),"""
""""failed authentication for user '(localhost|none|system|\.{3}|({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%\.]*:[A-Fa-f0-9%\.:]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^@.,']+(\.lan|\.local)?)|({email_address}[^@',]+@[^\.']+\.[^']+)|(({=domain}[^\\']+)\\)?({=user}[^']+))'""",
""""When authenticating user '(localhost|none|system|\.{3}|({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^@.,']+(\.lan|\.local)?)|({email_address}[^@',]+@[^\.']+\.[^']+)|({=user}[^']+))' from '(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-.]+))', ({failure_reason}[^.,]+)\.""",
"""Reason:\s*({failure_reason}[^\.]+)\.\s"""
"""From:\s*(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w\-\.]+?))\.?\""""
"""auth profile '({service_name}[^\']+)'"""
""",SYSTEM,(\"[^\"]+\",|[^,]*,){18}({host}[\w\-.]+)""",
"""((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
""",({serial_num}\d+),SYSTEM,auth"""
""",SYSTEM,([^,]*,){10}("[^"]+")?,([^,]*,){7}({device_name}({host}[^",]+))"""
  ]
  ParserVersion = "v1.0.0"


}
```