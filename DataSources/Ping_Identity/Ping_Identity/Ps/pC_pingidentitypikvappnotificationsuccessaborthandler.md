#### Parser Content
```Java
{
Name = pingidentity-pi-kv-app-notification-success-aborthandler
  ParserVersion = v1.0.0
  Conditions = [ """Invoking abort handler""", """pingidentity""" ]

ping-events-2 = {
  Vendor = Ping Identity
  Product = Ping Identity
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """sourceip="({src_ip}[a-fA-F:\d.]+)"""",
    """Request\sto\s\[({dest_ip}[A-Fa-f\d\.:]+?)(:({dest_port}\d+))?\]""",
    """({event_name}Invoking[^:]+):\s?({additional_info}[^\]]+\])"""
  
}
```