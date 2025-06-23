#### Parser Content
```Java
{
Name = "cyberark-pam-cef-app-activity-failed-undefined"
Vendor = "CyberArk"
Product = "CyberArk Privilege Access Manager"
TimeFormat = ["yyyy-MM-dd HH:mm:ss"]
Conditions = [
"""CEF:"""
""":undefined|"""
"""msg="""
"""Failure Description:"""
]
Fields = [
"""Error:\s*({error_info}[^:]+?)\s*\w+:""",
"""(C|c)ode:\s*({failure_code}\d+),"""
"""Failure Description:\s({failure_reason}[^:]+?)\s*\w+:"""
"""Object: ({additional_info}[^"\$]+?)\s*""""
"""to user ((({domain}[^\\]+)\\)?(-)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""\sSafe:\s*(\s+|({safe_value}[^=,]+))"""
]
ParserVersion = "v1.0.0"


}
```