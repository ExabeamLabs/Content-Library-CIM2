#### Parser Content
```Java
{
Name = "dell-sw-kv-vpn-login-fail-sslvpn"
Product = "Sonicwall"
Conditions = [
"""msg="User login failed"""
"""SSLVPN:"""
"""id=sslvpn"""
]
ParserVersion = "v1.0.0"

sonicwall-firewall.Fields} [
    """Category="({category}[^"]+)""",
    """dstname=(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({web_domain}[^"\/\s]+))"""
  
}
```