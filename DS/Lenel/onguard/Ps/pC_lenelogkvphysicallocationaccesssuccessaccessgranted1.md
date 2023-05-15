#### Parser Content
```Java
{
Name = lenel-og-kv-physical-location-access-success-accessgranted-1
    Vendor = Lenel
    Product = OnGuard
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """ EVDESCR: ""Access Granted"" """, """"" EMPID: """"" ]
    Fields = [
      """EVENT_LOCAL_TIME:\s*"+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
      """\sLASTNAME:\s*"+({last_name}[^"]+)""",
      """\sFIRSTNAME:\s*"+({first_name}[^"]+)""",
      """\sEVDESCR:\s*"+({result}[^"]+)""",
      """\sCARDNUM:\s*"+({badge_id}\d+)""",
      """\sEMPID:\s*"+({user}[^"]+)""",
      """\sREADERDESC:\s*"+({location_full}[^"]+)"""
    ]
    DupFields = [ "location_full->location_door" ]
    ParserVersion = "v1.0.0"
  

}
```