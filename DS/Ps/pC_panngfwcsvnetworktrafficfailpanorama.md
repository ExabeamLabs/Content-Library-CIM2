#### Parser Content
```Java
{
Name = pan-ngfw-csv-network-traffic-fail-panorama
    ParserVersion = v1.0.0
    Conditions = [
""",TRAFFIC,deny,""",
"""PANORAMA"""
    ]
    DupFields = [ "src_user->user", "src_domain->domain" ]


}
```