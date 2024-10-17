#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-login-fail-invaliduser-1"
Vendor = "Unix"
Product = "Unix"
TimeFormat = "yyyy MMM dd HH:mm:ss"
Conditions = [
""" <sshd> """
"""<Invalid user """
]
Fields = [
"""<({time}\d+\s+\w+\s+\d+\s+\d+:\d+:\d+)\s"""
"""({event_code}ssh)"""
"""<Invalid user ({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
""" from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\d+\s+\w+\s+\d+\s+\d+:\d+:\d+\s+\w+>\s+<({dest_host}[\w\-.]+)"""
]
ParserVersion = "v1.0.0"


}
```