#### Parser Content
```Java
{
Name = bitglass-casb-sk4-app-activity-success-onedrive
  ParserVersion = v1.0.0
  Conditions = [ """ api.bitglass.com """, """"filename":""", """"owner":""" ]

cef-bitglass-system-info = {
  Vendor = Bitglass
  Product = Bitglass CASB
  TimeFormat = "dd MMM yyyy HH:mm:ss"
  Fields = [
    """"time":"({time}\d+\s+\w+\s+\d+\s+\d+:\d+:\d+)""",
    """"application":"({app}[^"]+)"""",
    """"filename":"\s*({file_name}[^"]+?(\.({file_ext}[^\.\s"]+))?)\s*"""",
    """"owner":"({email_address}[^"]+)""",
    """"status":"({event_category}[^"]+)""",
    """"folder":"\s*({folder_name}[^"]+?)\s*"""",
    """"filelink":"({file_url}[^"]+)""",
    """"action":"({event_name}[^"]+?)"""",
  
}
```