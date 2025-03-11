#### Parser Content
```Java
{
Name = "dell-sw-kv-vpn-login-fail-140"
Product = "Sonicwall"
Conditions = [
""" m=140 """
"""id="""
""" usr="""
""" fw="""
"""Authentication failure"""
]
ParserVersion = "v1.0.0"

sonicwall-firewall.Fields} [
    """Category="({category}[^"]+)""",
    """dstname=(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({web_domain}[^"\/\s]+))"""
  
}
```