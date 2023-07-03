#### Parser Content
```Java
{
Name = juniper-ps-sk4-vpn-authentication-success-restrictionspassed
  ParserVersion = "v1.0.0"
  Conditions = [ """"host":""", """"PulseSecure:"""", """Certificate realm restrictions successfully passed""" ]
  Fields = ${JuniperParsersTemplates.cef-pulsesecure-vpn-events.Fields} [
    """Certificate realm restrictions successfully passed for\s+({user}[^\/]+)?\/({realm}[^\s]+) , with certificate \'({safe_value}[^\']+)\'""",
    """\'CN\\=({email_address}[^@',]+@[^,']+)"""
  ]

cef-pulsesecure-vpn-events = {
  Vendor = Ivanti
  Product = Ivanti Pulse Secure
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """"host":"({host}[^"]+)"""",
    """"timestamp":"({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """\- \[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s+([\w\s]+?::)?(({domain}[^\\\(]+)\\)?(System|({user}[^\(]+))\(({realm}[^\)]+)?\)\[({resource}[^\]]+)?\]""",
    """\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\s+\-\s+({dest_host}[\w\-.]+)"""
  
}
```