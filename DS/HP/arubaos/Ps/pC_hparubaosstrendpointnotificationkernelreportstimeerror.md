#### Parser Content
```Java
{
Name = hp-arubaos-str-endpoint-notification-kernelreportstimeerror
  ParserVersion = v1.0.0
  Product = ArubaOS
  Conditions = [ """ Aruba-HQ-Sec-Master """, """kernel reports TIME_ERROR""" ]

aruba-system-info-1 = {
    Vendor = HP
    Product = Aruba Mobility Master
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""",
      """"host":"(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({host}[^"]+))"""",
      """IP\\*=([a-fA-F\d.:]+:|N\/A) ({event_name}[^:,]+)""",
# bssid_mac is removed
# bssid_mac is removed
      """\|ids\|\s+({event_name}[^:]+):""",
      """({event_name}User Add message received for a client not allowed!|Authentication server request Timeout|CDR started for client)""",
      """\s+reason\\*=({result_reason}Station resetting role)""",
      """({channel}CHANNEL \d+)""",
# access_point is removed
# access_point is removed
# detector_access_point_name is removed
# detector_access_point_mac is removed
# detector_access_point_radio is removed
    
}
```