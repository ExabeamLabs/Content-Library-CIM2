#### Parser Content
```Java
{
Name = pan-gp-cef-vpn-login-gatewayauth
 ParserVersion = "v1.0.0"
 Conditions = [ """|gateway-auth|GLOBALPROTECT|""", """GLOBALPROTECT""", ]
 Fields = ${PaloAltoParsersTemplates.paloalto-vpn-login.Fields}[
    """({event_name}gateway-auth)"""
  ]

paloalto-vpn-login = {
  Vendor = Palo Alto Networks
  Product = GlobalProtect
  TimeFormat = "MMM dd yyyy HH:mm:ss zzz"
  Fields = [
    """GPClientHostName =(|({host}[\w.-]*?))\s+\w+?=""",
    """rt=({time}\w{3}\s\d{2}\s\d{4}\s(\d{2}:){2}\d{2}\s\S{3})\s""",
    """GPClientPrivateIPv4=({src_translated_ip}[A-Fa-f0-9.:]+)""",
    """ClientPublicIPv4=({src_ip}[A-Fa-f0-9.:]+)""",
    """GPSourceUser=(({domain}[^\\\s,]+)\\+)?({user}[^\\\s,]+)""",
    """dvchost=({src_host}[\w.-]+?)\s""",
    """GPClientOS=(|({os}[^=]*?))(\s+)?\w+?=""",
    """msg="({additional_info}[^"]+?)"""",
    """GPStatus=({result}\S+?)\s""",
    """({app}GLOBALPROTECT)"""
  
}
```