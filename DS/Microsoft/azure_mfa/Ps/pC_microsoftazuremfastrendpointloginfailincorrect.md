#### Parser Content
```Java
{
Name = "microsoft-azuremfa-str-endpoint-login-fail-incorrect"
ParserVersion = "v1.0.0"
Vendor = "Microsoft"
Product = "Azure MFA"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""|validate_oath_code: user """
""" pfsvc: """
"""updated authentication result."""
"""callStatus = OATH Code Incorrect"""
]
Fields = [
"""\w{3}\s\d\d\s\d\d:\d\d:\d\d\s({host}[^\s]+)\spfsvc:""",
"""({event_name}validate_oath_code)""",
"""({failure_reason}OATH Code Incorrect)""",
    """user\s+(({email_address}[^@\s]+@[^\s]+)|(({domain}[^\\\s']+)\\)?({user}[^\s']+))\s+updated"""
    ]


}
```