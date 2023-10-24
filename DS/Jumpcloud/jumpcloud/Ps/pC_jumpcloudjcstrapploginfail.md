#### Parser Content
```Java
{
Name = jumpcloud-jc-str-app-login-fail
   Vendor = Jumpcloud
   Product = Jumpcloud
   ParserVersion = "v1.0.0"
   TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
   Conditions = [ """User """, """ failed to login """, """, process name: """, """, caused by """, """, time: """ ]
   Fields = [
     """time:\s+({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d{1,7}Z)""",
     """User\s+(-|(({email_address}[^@"]+@({email_domain}[^\."]+\.[^"]+?))|({user}[\w\.\-]{1,40}\$?)|({full_name}[^~"]+?)))\s+({event_name}failed to login)""",
     """process name:\s+(-|({process_path}[^,]+?)),\s""",
     """caused by ({failure_reason}[^,]+?),""",
   ]


}
```