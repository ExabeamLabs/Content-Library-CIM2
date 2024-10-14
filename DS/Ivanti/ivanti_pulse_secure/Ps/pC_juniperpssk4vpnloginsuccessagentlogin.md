#### Parser Content
```Java
{
Name = juniper-ps-sk4-vpn-login-success-agentlogin
  ParserVersion = "v1.0.0"
  Conditions = [ """"host":""", """"PulseSecure:"""", """Agent login succeeded for""" ]
  Fields = ${JuniperParsersTemplates.cef-pulsesecure-vpn-events.Fields} [
    """\[\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}\][^\[]+?\[({resource}[^\]]+)\]""",
    """({event_code}Agent login succeeded) for ({user}[\w\.\-\!\#\^\~]{1,40}\$?)(?:@({domain}[^\/]+))?.+? from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """({os}iOS|Android|BlackBerry|iPhone OS|Windows Phone|BeOS|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin)"""
  ]

cef-pulsesecure-vpn-events = {
  Vendor = Ivanti
  Product = Ivanti Pulse Secure
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ssZ", "yyyy-MM-dd HH:mm:ss"]
  Fields = [
    """"host":"({host}[^"]+)"""",
    """({time}\d{4}-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """"timestamp":"({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d+:\d+)""",
    """\- \[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s+([\w\s]+?::)?(({domain}[^\\\(]+)\\)?(System|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\(({realm}[^\)]+)?\)\[({resource}[^\]]+)?\]""",
    """\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\s+\-\s+({dest_host}[\w\-.]+)"""
  
}
```