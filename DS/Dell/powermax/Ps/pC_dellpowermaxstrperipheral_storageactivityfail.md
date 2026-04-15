#### Parser Content
```Java
{
Name = "dell-powermax-str-peripheral_storage-activity-fail"
    Vendor = "Dell"
    Product = "PowerMax"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    ParserVersion = "v1.0.0"
    Conditions = ["""EMCstorevntd:""","""[evtid=""","""[sev=""" ]
    Fields = [
        """\[evtid=({event_id}\d+)\]""",
        """\[date=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
        """\[symid=({device_id}\d+)\]""",
        """\[sev=({severity}\w+)\]\s*=\s*({error_info}.*)"""
    ]


}
```