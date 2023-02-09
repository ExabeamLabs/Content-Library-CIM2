#### Parser Content
```Java
{
Name = hp-arubamm-cef-app-notification-appnotification
   ParserVersion = v1.0.0
   Vendor = HP
   Product = Aruba Mobility Master
   TimeFormat = "yyyy-MM-dd HH:mm:ss"
   Conditions = [ """CEF:""", """|Aruba|MM|""", """|SystemEvent|""", """Interfering AP:""" ]
   Fields = [
     """dvchost=({host}[^\s]+)""",
     """CEF:\d+\s*\|([^|]*\|){5}({alert_severity}\d+)""",
     """CEF:\d+\s*\|([^|]*\|){2}({alert_type}\d+)""",
     """Interfering AP:\s+({event_name}[^=]+)\s+\(""",
# detector_access_point_ratio is removed
# detector_access_point_mac is removed
# detector_access_point_name is removed
# bssid_mac is removed
     """CHANNEL\s({channel}\d+)""",
     """\sSSID\s+(\s|NONE|({ssid}.+?))\s*on CHANNEL"""
    ]


}
```