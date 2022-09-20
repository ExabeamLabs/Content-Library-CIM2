#### Parser Content
```Java
{
Name = citrix-netscaler-cef-vpn-login-success-login
  Vendor = Citrix
  Product = Citrix Netscaler VPN
  TimeFormat = "epoch"
  Conditions = [ """|Citrix|NetScaler|""","""LOGIN|""" ]
  Fields = [
    """\srt=({time}\d+)""",
    """\sClient_ip\s+({src_ip}[\d\.a-fA-F:]+)\s""",
    """\ssrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\s(s|d)user=({user}.+?)\s+\w+=""",
    """\sdst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sshost=({src_host}[^\s]+)""",
    """\sdhost=({src_host}[^\s]+)""",
    """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sdvchost=({host}[^\s]+)""",
    """SessionId:\s+({session_id}\d+)""",
    """cn1=({session_id}\d+)""",
    """Browser_type "+({user_agent}[^"]+)""",
    """Browser_type\s*({user_agent}[^\-]+?)\s*\-""",
    """requestClientApplication=({user_agent}.+?)\s+\w+=""",
    """SSLVPN_client_type\s*({vpn_client_type}[^\-]+?)\s\-""",
    """Group\(s\) "+(N\/A|({realm}[^"]+))""",
    """ Nat_ip ({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
  ]
  DupFields = ["user->account"]
  ParserVersion = "v1.0.0"


}
```