#### Parser Content
```Java
{
Name = "securecomputing-safeword-kv-endpoint-authentication-success-authverify"
Vendor = "Secure Computing"
Product = "Secure Computing SafeWord"
TimeFormat = "epoch"
Conditions = [
"""|SecureComputing|SafeWord PremierAccess|"""
"""categoryBehavior=/Authentication/Verify"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""cs4=\d+/\d+/\d+ \d+:\d+:\d+.\d+ \(\w+\) ({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
"""\ssuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
"""\sshost=({src_host}[^\s]+)"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```