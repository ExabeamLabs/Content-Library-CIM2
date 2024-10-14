#### Parser Content
```Java
{
Name = "entrust-ie-kv-endpoint-login-fail-authfailforuser"
Vendor = "Entrust"
Product = "Entrust Identity Enterprise"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""] Failed authentication for user """
"""Invalid response to a challenge."""
""" authentication attempts remaining."""
]
Fields = [
"""\[({time}\d{4}-\d\d-\d\d \d\d:\d\d:\d\d)(\]|,\]|,\d+\])"""
""" user (({email_address}[^\@\s]+@[^\s]+)|(({domain}[^\\\/]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\. """
"""({additional_info}Invalid response to a challenge.[^\.]+)"""
]
ParserVersion = "v1.0.0"


}
```