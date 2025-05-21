#### Parser Content
```Java
{
Name = "f5-bigip-kv-ssh-traffic-success-sshd"
   ParserVersion = "v1.0.0"
   Vendor = "F5"
   Product = "F5 BIG-IP"
   TimeFormat = ["MMM dd HH:mm:ss yyyy","MMM d HH:mm:ss yyyy"]
   ExtractionType = json
   Conditions = [ 
"""pam_audit"""
""" tty="""
"""attempts="""
]
   Fields = [
"""host=({host}(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))|({src_host}[\w\-\.]+))\s\w+="""
"""\w{3}\s+\d{1,2}\s\d\d:\d\d:\d\d\s({host}\S+)\sinfo"""
"""start=\\?"\w+\s({time_started}\w+\s*\d+\s\d\d:\d\d:\d\d\s\d\d\d\d)"""
"""end=\\?"\w+\s({time_ended}\w+\s*\d+\s\d\d:\d\d:\d\d\s\d\d\d\d)"""
"""end=\\?"\w+\s({time}\w+\s*\d+\s\d\d:\d\d:\d\d\s\d\d\d\d)"""
"""(?:u|U)ser=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\("""
"""\s({protocol}\w+)\(pam_audit\)\["""
"""exa_regex=host=({host}(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))|({src_host}[\w\-\.]+))\s\w+="""
"""exa_regex=\w{3}\s+\d{1,2}\s\d\d:\d\d:\d\d\s({host}\S+)\sinfo"""
"""exa_json_path=$._raw,exa_regex=start=\\?"\w+\s({time_started}\w+\s*\d+\s\d\d:\d\d:\d\d\s\d\d\d\d)"""
"""exa_json_path=$._raw,exa_regex=end=\\?"\w+\s({time_ended}\w+\s*\d+\s\d\d:\d\d:\d\d\s\d\d\d\d)"""
"""exa_json_path=$._raw,exa_regex=end=\\?"\w+\s({time}\w+\s*\d+\s\d\d:\d\d:\d\d\s\d\d\d\d)"""
"""exa_regex=(?:u|U)ser=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\("""
"""exa_regex=\s({protocol}\w+)\(pam_audit\)\["""
   ]


}
```