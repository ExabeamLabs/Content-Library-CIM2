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
  """\smsg="({alert_subject}[^:"-]+?)\s*(:|"|-)"""
  
}
```