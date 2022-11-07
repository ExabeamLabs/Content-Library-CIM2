#### Parser Content
```Java
{
Name = citrix-netscaler-str-vpn-logout-success-logout
  ParserVersion = v1.0.0
  Vendor = Citrix
  Product = Citrix Netscaler VPN
  TimeFormat = "MM/dd/yyyy:HH:mm:ss"
  Conditions = [ """SSLVPN LOGOUT""", """ Client_ip """ ]
  Fields = [
    """\w+\s+\d+\s+\d\d:\d\d:\d\d\s+({host}[\w\-.]+)""",
    """({time}\d\d/\d\d/\d\d\d\d:\d\d:\d\d:\d\d)\s+({host}(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[^\s]+)))""",
    """User ({email_address}[^@\s]+@[^@\s]+) - Client_ip ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """User (({domain}[^\\\/\s@]+)[\\\/]+)?({user}[^@\s]+) - Client_ip ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """ Nat_ip ({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """ SSLVPN_client_type ({vpn_client_type}[^\s]+) -"""
  ]


}
```