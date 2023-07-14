#### Parser Content
```Java
{
Name = microsoft-azureatp-json-alert-trigger-success-netlogonbypasssecurityalert
Product = "Azure ATP"
Conditions = [
  """"category":"""
  """"NetlogonBypassSecurityAlert""""
  """"title":"""
  """"vendor":"""
  """"Microsoft""""
  """"provider":"""
  """"Azure Advanced Threat Protection""""
]
ParserVersion = "v1.0.0"

defender-atp-events.Fields} [
  """"AccountName":"((email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))"""
  
}
```