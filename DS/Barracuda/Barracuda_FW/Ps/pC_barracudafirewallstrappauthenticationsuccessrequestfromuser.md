#### Parser Content
```Java
{
Name = barracuda-firewall-str-app-authentication-success-requestfromuser
  ParserVersion = v1.0.0
  Conditions = [ """Session PHS: Authentication request from user""", """VPN""" ]
  Fields = ${BarracudaParserTemplates.barracuda-vpn-auth-attempt.Fields} [
    """request from user (({email_address}[^@\s\(]+@[^\s\(@]+)|({user}[^\s]+))""",
    """({event_name}Authentication request from user)""",
  ]

barracuda-vpn-auth-attempt = {
  Vendor = Barracuda
  Product = Barracuda FW
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """Info\s+({host}[^\s:]+)\s+Session""",
    """\W(login|user)=(({email_address}[^@\s\(]+@[^\s\(@]+)|({user}[^\s\(]+))\s*\(({src_ip}[A-Fa-f:\d.]+?):({src_port}\d+)""",
    """\W((?i)(login|user))=(({email_address}[^@\s\(]+@[^\s\(@]+)|({user}[^\s\(=]+))""",
    """user '(({email_address}[^'@\s\(]+@[^'\s\(@]+)|({user}[^'\s\(=]+))\s*'""",
    """Session PHS:\s*({event_name}[^:=\(]+?)\s*(:|\w+=|\(|$)""",
    """((?i)scheme)=({auth_method}[^\s=]+)"""  
  
}
```