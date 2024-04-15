#### Parser Content
```Java
{
Name = "amazon-awabastion-str-endpoint-login-fail-accessdeniedtoidqsadsgui"
Vendor = "Amazon"
Product = "AWS Bastion"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""" bastion"""
"""denied access"""
]
Fields = [
"""\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+bastion"""
"""({event_name}denied access)"""
"""bastion\d*:({hostname}[^:]+):({user}[^:]+):\s"""
""":\s+({failure_reason}.+?)\s*$"""
]
ParserVersion = "v1.0.0"


}
```