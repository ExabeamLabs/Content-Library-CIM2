#### Parser Content
```Java
{
Name = "citrix-cgateway-str-app-login-success-sslvpnlogin"
  Vendor = "Citrix"
  Product = "Citrix Gateway"
  TimeFormat = "MM/dd/yyyy:HH:mm:ss"
  Conditions = [
    """SSLVPN LOGIN"""
    """ Client_ip """
  ]
  Fields = [
    """\w+\s+\d+\s+\d\d:\d\d:\d\d\s+({host}[\w\-.]+)\s"""
    """({time}\d\d/\d\d/\d\d\d\d:\d\d:\d\d:\d\d)"""
    """User (({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|((({domain}[^\\\/]+?)(?:\\|\/))?({user}[\w\.\-\!\#\^\~]{1,40}\$?))) - Client_ip ({host}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
    """dvchost=({host}[^\s]+)"""
    """User (({domain}[^@\s\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?) - Client_ip ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """ Nat_ip ({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
    """SSLVPN_client_type\s*({app}({vpn_client_type}[^\s]+)) - Group"""
    """Browser_type (\")+(?:-|({user_agent}[^\"]+))"""
    """Vserver\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  ]
  ParserVersion = "v1.0.0"


}
```