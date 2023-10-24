#### Parser Content
```Java
{
Name = citrix-cgateway-str-vpn-logout-success-logout
  ParserVersion = v1.0.0
  Vendor = Citrix
  Product = Citrix Gateway
  TimeFormat = "MM/dd/yyyy:HH:mm:ss"
  Conditions = [ """SSLVPN LOGOUT""", """ Client_ip """ ]
  Fields = [
    """\w+\s+\d+\s+\d\d:\d\d:\d\d\s+({host}[\w\-.]+)""",
    """({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d)\s+(\w\w\w)?\s+({host}(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[^\s]+)))""",
    """User ({email_address}[^@\s]+@[^@\s]+) - Client_ip ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """User (({domain}[^\\\/\s@]+)[\\\/]+)?({user}[\w\.\-]{1,40}\$?) - Client_ip ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """ Nat_ip ({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """ SSLVPN_client_type ({vpn_client_type}[^\s]+) -""",
    """Total_bytes_send ({bytes_out}\d+)\s*-""",
    """SessionId.*?Duration ({session_duration}[^\s]+)\s-"""
  ]


}
```