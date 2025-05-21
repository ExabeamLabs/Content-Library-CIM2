#### Parser Content
```Java
{
Name = pingidentity-pi-kv-app-notification-success-aborthandler
  ParserVersion = v1.0.0
  Conditions = [ """Invoking abort handler""", """pingidentity""" ]

ping-events-2 = {
  Vendor = Ping Identity
  Product = Ping Identity
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ","yyyy-MM-dd'T'HH:mm:ss"]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """sourceip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """Request\sto\s\[({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\]""",
    """({event_name}Invoking[^:]+):\s?({additional_info}[^\]]+\])"""
  
}
```