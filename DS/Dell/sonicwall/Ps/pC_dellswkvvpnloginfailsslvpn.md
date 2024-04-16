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
  """\smsg="({alert_subject}[^:"-]+?)\s*(:|"|-)"""
  
}
```