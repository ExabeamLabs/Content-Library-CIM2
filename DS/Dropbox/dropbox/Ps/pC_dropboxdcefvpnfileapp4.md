#### Parser Content
```Java
{
Name = dropbox-d-cef-vpnfileapp-4
  ParserVersion = "v1.0.0"
  Conditions = [ """destinationServiceName =Dropbox""", """.tag""", """"access_method"""",  """"devices"}""" ]

cef-dropbox-activity = {
  Vendor = Dropbox
  Product = Dropbox
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
    """\w+\s+\d+\s+\d\d:\d\d:\d\d ({host}[\w\-.]+) \d+ \d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ""",
    """"timestamp":\s*"({time}[^"]+)""",
    """"host_name":\s*"({host}[^"]+)""",
    """"actor":\s*[^\}]*?"display_name":\s*"(?:N\/A|({full_name}[^"@]+))"""",
    """"actor":\s*[^\}]*?"email":\s*"(?:N\/A|({email_address}[^@"\s]+@[^@"\s]+))"""",
    """"event_type":\s*"({operation}[^"]+)"""",
    """"event_type":\s*\{("description":\s*"[^"]+",\s*)?"\.tag":\s*"({operation}[^"]+)"""",
    """"description":\s*"({additional_info}[^"]+)"""",
    """"ip_address":\s*"({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+))""",
    """({app}Dropbox)""",
  
}
```