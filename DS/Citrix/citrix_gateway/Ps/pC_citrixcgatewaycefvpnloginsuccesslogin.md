#### Parser Content
```Java
{
Name = citrix-cgateway-cef-vpn-login-success-login
  Vendor = Citrix
  Product = Citrix Gateway
  TimeFormat = "epoch"
  Conditions = [ """|Citrix|NetScaler|""","""LOGIN|""" ]
  Fields = [
    """\srt=({time}\d{13})""",
    """\sClient_ip\s+({src_ip}[\d\.a-fA-F:]+)\s""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\s(s|d)user=({user}.+?)\s+\w+=""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sshost=({src_host}[^\s]+)""",
    """\sdhost=({dest_host}[^\s]+)""",
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