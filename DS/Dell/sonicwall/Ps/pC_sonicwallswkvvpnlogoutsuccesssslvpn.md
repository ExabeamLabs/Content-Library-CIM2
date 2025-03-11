#### Parser Content
```Java
{
Name = "sonicwall-sw-kv-vpn-logout-success-sslvpn"
Product = "Sonicwall"
Conditions = [
  """msg="User logged out"""
  """SSLVPN:"""
  """id=sslvpn"""
]
ParserVersion = "v1.0.0"

sonicwall-firewall.Fields} [
    """Category="({category}[^"]+)""",
    """dstname=(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({web_domain}[^"\/\s]+))"""
  
}
```