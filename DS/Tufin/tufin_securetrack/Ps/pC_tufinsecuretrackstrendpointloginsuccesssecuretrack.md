#### Parser Content
```Java
{
Name = "tufin-securetrack-str-endpoint-login-success-securetrack"
Product = "Tufin SecureTrack"
Vendor = "Tufin"
TimeFormat = "yyyy.MM.dd HH:mm:ss.SSS"
Conditions = [
"""ELM"""
"""SecureTrack:"""
]
Fields = [
"""timestamp:({time}\d+.\d+.\d+ \d+:\d+:\d+)"""
"""({host}[^\s]+)\s+SecureTrack:"""
"""Login was done by\s+({user}[\w\.\-]{1,40}\$?)\.,"""
]
ParserVersion = "v1.0.0"


}
```