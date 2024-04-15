#### Parser Content
```Java
{
Name = "f5-bigip-kv-ssh-traffic-success-sshd"
   ParserVersion = "v1.0.0"
   Vendor = "F5"
   Product = "F5 BIG-IP"
   TimeFormat = "yyyy-MM-dd HH:mm:ss"
   Conditions = [ 
"""pam_audit"""
""" tty="""
"""attempts="""
]
   Fields = [
"""\w{3}\s\d\d\s\d\d:\d\d:\d\d\s({host}\S+)\sinfo"""
"""start=\"\w+\s({time_started}\w+\s*\d+\s\d\d:\d\d:\d\d\s\d\d\d\d)"""
"""end=\"\w+\s({time_ended}\w+\s*\d+\s\d\d:\d\d:\d\d\s\d\d\d\d)"""
"""host=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\sattempts="""
"""(?:u|U)ser=({user}[^\s\(]+)""",
"""host=({host}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})"""
"""\s({protocol}\w+)\(pam_audit\)\["""
   ]


}
```