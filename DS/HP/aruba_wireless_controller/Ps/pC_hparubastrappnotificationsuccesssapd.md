#### Parser Content
```Java
{
Name = hp-aruba-str-app-notification-success-sapd
  Vendor = HP
  Product = Aruba Wireless controller
  ParserVersion = v1.0.0
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """ sapd[""", """An internal system error has occurred""" ]
  Fields = [
    """({time}\w{3}\s+\d{2}\s+\d{2}:\d{2}:\d{2}\s+\d{4})\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\ssapd\[""",
    """sapd\|\s*({additional_info}An internal system error has occurred at file messenger.[^=]+?)\s({event_name}Unable to get [^"]+)\s(for|on interface)\s({src_interface}\S+?)\."""
  ]


}
```