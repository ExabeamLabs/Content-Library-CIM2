#### Parser Content
```Java
{
Name = "pan-ngfw-cef-vpn-login-success-clientswitchtossltunnelmodesucceeded"
Conditions = [
"""|Palo Alto Networks|PAN-OS|"""
"""|client switch to SSL tunnel mode succeeded|"""
]
ParserVersion = "v1.0.0"

leef-paloalto-vpn-event.Fields}[
      """usrName =(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^\\\s,]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
      
}
```