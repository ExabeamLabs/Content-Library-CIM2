#### Parser Content
```Java
{
Name = "juniper-srx-cef-vpn-login-success-loginsucceededfor"
Conditions = [
"""CEF:"""
"""|McAfee|ESM|"""
"""|Login succeeded for|"""
]
ParserVersion = "v1.0.0"

cef-pulsesecure-vpn-events.Fields} [
    """Session ended for user with IPv4 address ({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  
}
```