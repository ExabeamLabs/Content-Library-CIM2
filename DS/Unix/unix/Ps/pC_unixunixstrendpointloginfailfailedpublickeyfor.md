#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-login-fail-failedpublickeyfor"
Vendor = "Unix"
Product = "Unix"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""]["""
""" sshd """
""" Failed publickey for """
]
Fields = [
"""<\d+>\d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d) ({host}[\w.\-]+) ({event_code}sshd)"""
"""({failure_reason}Failed publickey) for (({domain}[^\\]+?)\\+)?({user}[^\\]+?) from """
"""\sfrom ({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sport ({src_port}\d+)"""
]
ParserVersion = "v1.0.0"


}
```