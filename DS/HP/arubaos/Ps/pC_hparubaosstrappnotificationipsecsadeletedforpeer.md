#### Parser Content
```Java
{
Name = hp-arubaos-str-app-notification-ipsecsadeletedforpeer
  ParserVersion = v1.0.0
  Product = ArubaOS
  Conditions = [ """ Aruba-HQ-Sec-Master """, """IPSEC SA deleted for peer""" ]

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
    aruba-system-info = {
  Vendor = HP
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Fields = [
    """({time}\w+\s+\d+\s+\d+:\d+:\d+\s+\d+)\s+Aruba-HQ-Sec-Master""",
    """({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?>\s+ntpd\[\d+\]:\s*({event_name}.+?)\s*$"""
    """<Aruba-HQ-Sec-Master\s+({src_ip}((([9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?>\s*({event_name}.+?)\s*$""",
  ]
}
}
```