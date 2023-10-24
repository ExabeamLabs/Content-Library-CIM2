#### Parser Content
```Java
{
Name = dropbox-d-cef-vpnfileapp-4
  ParserVersion = "v1.0.0"
  Conditions = [ """"team_member_id":"dbmid:""", """.tag""", """"access_method"""",  """"devices"}""" ]

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
    """"ip_address":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """({app}Dropbox)""",
  
}
```