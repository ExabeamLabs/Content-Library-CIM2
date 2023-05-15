#### Parser Content
```Java
{
Name = lenel-og-kv-physical-location-access-success-accessgranted
  Vendor = Lenel
  Product = OnGuard
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss.S"
  Conditions = [ """ EVENT_TIME_UTC=""", """"Access Granted"""", """EVTDESCR=""", """READERDESC=""" ]
  Fields = [
    """EVTDESCR="*({action}[^"]+)"*""",
    """EVENT_TIME_UTC="*({time}\d{4}-\d{2}-\d{2}\s\d{2}:\d{2}:\d{2}\.\d+)"*""",
    """FIRSTNAME="*({first_name}[^"]+)"*""",
    """LASTNAME="*({last_name}[^"]+)"*""",
    """CARDNUM="*({badge_id}\d+)"*""",
    """EMPID="*({employee_id}[^"]\d+)"*""",
    """\sNAME="*({location_building}[^"]+)"*""",
    """READERDESC="*({location_door}[^"]+)"*""",
    """SERIALNUM="*({serial_num}[^"]+)"*"""
  ]


}
```