#### Parser Content
```Java
{
Name = juniper-ps-sk4-vpn-login-fail-authloginfailed
  ParserVersion = v1.0.0
  Conditions = [ """"host":""", """"PulseSecure:"""", """Login failed using auth server""", """Reason:""" ]
  Fields = ${JuniperParsersTemplates.cef-pulsesecure-vpn-events.Fields} [
    """Reason:\s+({failure_reason}[^"]+?)\s*"""",
    """\- \[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s+([\w\s]+?::)?(({domain}[^\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\(({realm}[^\)]+)?\)\[([^\-]*)\-\s*({failure_reason}[^\:\.]+)?\s*"""
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