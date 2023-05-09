#### Parser Content
```Java
{
Name = lenel-og-kv-physical-location-access-accessgranted-2
  Vendor = Lenel
  Product = OnGuard
  TimeFormat =  "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ EVDESCR: """", """ USERID: """", """ PANELNAME: """", """ READERDESC: """" ]
  Fields = [
    """EVENT_TIME_UTC:\s*"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """\sLASTNAME:\s*"({last_name}[^"]+)""",
    """FIRSTNAME:\s*"({first_name}[^"]+)""",
    """\sEVDESCR:\s*"({result}[^"]+)""",
    """\sUSERID:\s*"({badge_id}[^"]+)""",
    """\sREADERDESC:\s*"({location_door}[^"]+)""",
    """PANELNAME:\s*"({location_building}[^"]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```