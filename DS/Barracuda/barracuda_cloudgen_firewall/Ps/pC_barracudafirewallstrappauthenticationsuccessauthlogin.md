#### Parser Content
```Java
{
Name = barracuda-firewall-str-app-authentication-success-authlogin
  ParserVersion = v1.0.0
  Conditions = [ """Session PHS: Retransmission Authentication Login""", """VPN""" ]

barracuda-vpn-auth-attempt = {
  Vendor = Barracuda
  Product = Barracuda Cloudgen Firewall
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """Info\s+({host}[^\s:]+)\s+Session""",
    """\W(login|user)=(({email_address}[^@\s\(]+@[^\s\(@]+)|({user}[\w\.\-]{1,40}\$?))\s*\(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))""",
    """\W((?i)(login|user))=(({email_address}[^@\s\(]+@[^\s\(@]+)|({user}[\w\.\-]{1,40}\$?))""",
    """user '(({email_address}[^'@\s\(]+@[^'\s\(@]+)|({user}[\w\.\-]{1,40}\$?))\s*'""",
    """Session PHS:\s*({event_name}[^:=\(]+?)\s*(:|\w+=|\(|$)""",
    """((?i)scheme)=({auth_method}[^\s=]+)"""  
  
}
```