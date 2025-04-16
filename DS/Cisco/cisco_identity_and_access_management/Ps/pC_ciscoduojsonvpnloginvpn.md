#### Parser Content
```Java
{
Name = cisco-duo-json-vpn-login-vpn
  Vendor = Cisco
  Product = "Cisco Identity and Access Management"
  TimeFormat = "epoch_sec"
  ParserVersion = "v1.0.0"
  Conditions = [ """"event_type":"""", """"result":""", """"user":""", """"access_device":""", """VPN""" ]
  Fields = [
    """"timestamp":({time}\d{10})""",
    """"host(name)?":"+({host}[\w\-\.]+)"""",
    """"ip":"+(0.0.0.0|null|({src_ip}[a-fA-F:\.\d]+))"""",
    """"result":"({result}[^"]+)"""",
    """"reason":"({failure_reason}[^"]+)"[^=]+?"result":"(denied|fraud|failure|error)"""",
    """"result":"(denied|fraud|failure|error)"[^=]+?"reason":"({failure_reason}[^"]+)"""",
    """"os":"({os}[^"]+)"""",
    """"os_version":"({os_version}[^"]+)"""",
    """"browser":"(Unknown|({browser}[^"]+))"""",
    """"browser_version":"({browser_version}[^"]+)"""",
    """"email":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
    """"factor":"(?:n\/a|({factor}[^"]+))"""",
    """"user":[^\}]+?"name":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
    """"application".+?"name":\s*"({service_name}[^"]+)"""
    """"location":.+?"country":\s*"({src_country}[^"]+)"""
    """"access_device":.+?"hostname":"({mfa_device}[^"]+)"""
    """"event_type":"({event_name}[^"]+)""""   
  ]
   DupFields = ["src_country->mfa_country"]


}
```