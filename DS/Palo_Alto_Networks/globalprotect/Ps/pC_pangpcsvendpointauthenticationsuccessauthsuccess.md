#### Parser Content
```Java
{
Name = "pan-gp-csv-endpoint-authentication-success-authsuccess"
  Vendor = "Palo Alto Networks"
  Product = "GlobalProtect"
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [
""",SYSTEM,auth,""",
""",auth-success,"""
  ]
  Fields = [
"""SYSTEM,auth,[^,]+,({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z),"""
""":\d\d:\d\d\s+({host}[\w.-]+)\s"""
"""\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+\d+,({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+),"""
""",auth-success,({auth_method}[^,]+)"""
"""\suser '(({user}[^@',]+)@({domain}[^@.,']+\.lan)|({email_address}[^@\s']+@[^.']+\.[^']+)|(({=domain}[^\s'\\]+)\\+)?({=user}[^\s']+))'""",
""""authenticated for user '(({email_address}[^@\s']+@[^\.']+\.[^']+)|(({domain}[^\s'\\]+)\\+)?({user}[^\s']+))""",
"""From:\s*(({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)|({src_host}.+?))\.?\""""
"""({event_name}auth-success)"""
"""auth-success,([^,]*,){5}\"?({additional_info}[^,']+?)\s'"""
""",SYSTEM,(\"[^\"]+\",|[^,]*,){18}({dest_host}[\w\-.]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```