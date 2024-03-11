#### Parser Content
```Java
{
Name = pan-ngfw-csv-network-traffic-fail-drop
    ParserVersion = v1.0.0
    TimeFormat = "yyyy/MM/dd HH:mm:ss"
    Conditions = [
""",TRAFFIC,drop,"""
    ]
    DupFields = [ "src_user->user" ]


}
```