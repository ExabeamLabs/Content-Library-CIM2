#### Parser Content
```Java
{
Name = "ncp-n-str-app-authentication-fail-verificationfailed"
Vendor = "NCP"
Product = "NCP"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""(VPN) PKI: Verification failed!"""
]
Fields = [
"""<.+?>\w+ \d+ \d\d:\d\d:\d\d ({host}\S+)"""
"""\[?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^\s@\]]+))?\]?\s+\S+\s+\(VPN\) PKI: Verification failed!\s*({failure_reason}[^\.]+)(\.|\s*$)"""
]
ParserVersion = "v1.0.0"


}
```