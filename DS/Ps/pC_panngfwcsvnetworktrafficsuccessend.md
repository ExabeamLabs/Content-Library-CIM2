#### Parser Content
```Java
{
Name = pan-ngfw-csv-network-traffic-success-end
    ParserVersion = v1.0.0
    Conditions = [
""",TRAFFIC,""",
""",allow,"""
    ]
    Fields = ${PaloAltoParsersTemplates.paloalto-firewall.Fields}[
    """TRAFFIC,([^,]*,){10}({action}(incomplete|insufficient-data))\s*"""
    ]


}
```