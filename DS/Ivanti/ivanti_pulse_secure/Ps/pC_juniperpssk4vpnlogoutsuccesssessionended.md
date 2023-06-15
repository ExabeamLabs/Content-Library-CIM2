#### Parser Content
```Java
{
Name = juniper-ps-sk4-vpn-logout-success-sessionended
  ParserVersion = "v1.0.0"
  Conditions = [ """"host":""", """"PulseSecure:"""", """VPN Tunneling: Session ended for user""" ]
  Fields = ${JuniperParsersTemplates.cef-pulsesecure-vpn-events.Fields} [
    """Session ended for user with IPv4 address ({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  ]

cef-pulsesecure-vpn-events = {
  Vendor = Ivanti
  Product = Ivanti Pulse Secure
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """"host":"({host}[^"]+)"""",
    """"timestamp":"({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """\- \[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s+(?:Default Network|Root)::(({domain}[^\\\(]+)\\)?(System|({user}[^\(]+))\(({realm}[^\)]+)?\)\[({resource}[^\]]+)?\]""",
    """\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\s+\-\s+({dest_host}[\w\-.]+)"""
  
}
```