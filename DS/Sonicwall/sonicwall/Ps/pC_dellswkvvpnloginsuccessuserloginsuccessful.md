#### Parser Content
```Java
{
Name = "dell-sw-kv-vpn-login-success-userloginsuccessful"
Product = "Sonicwall"
Conditions = [
"""msg="User login successful""""
"""SSLVPN:"""
"""id=sslvpn"""
]
ParserVersion = "v1.0.0"

sonicwall-firewall.Fields} [
  """\smsg="({alert_subject}[^:"-]+?)\s*(:|"|-)"""
  
}
```