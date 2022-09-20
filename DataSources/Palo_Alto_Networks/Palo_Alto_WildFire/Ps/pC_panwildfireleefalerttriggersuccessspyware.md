#### Parser Content
```Java
{
Name = pan-wildfire-leef-alert-trigger-success-spyware
  Conditions = [ """|Palo Alto Networks|PAN-OS""", """|Subtype=spyware|""" ]
  ParserVersion = "v1.0.0"

leef-pan-alert = {
  Vendor = Palo Alto Networks
  Product = Palo Alto WildFire
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Fields = [
    """ReceiveTime=({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)""",
    """({host}[\w\.-]+)(\s+|,"+)LEEF:""",
    """\|DeviceName =({host}[^\|"]+?)\s*(\||"*$)""",
    """\|Subtype=({alert_type}[^\|]+)""",
    """\|src=({src_ip}[a-fA-F\d.:]+)""",
    """\|dst=({dest_ip}[a-fA-F\d.:]+)""",
    """\|Application=({process_name}[^\|]+)""",
    """\|srcPort=({src_port}\d+)""",
    """\|dstPort=({dest_port}\d+)""",
    """\|proto=({protocol}[^\|]+)""",
    """\|action=({action}[^\|]+)""",
    """\|Miscellaneous="({additional_info}[^"\|]+)"""",
    """\|ThreatID=({alert_name}[^\|]+)""",
    """\|URLCategory=({category}[^\|]+)""",
    """\|Severity=({alert_severity}[^\|]+)""",
    """\|ThreatCategory=(?:unknown|({threat_category}[^\|]+))""",
    """usrName =({domain}[^\\\|]+)\\({user}[^\s\|]+)""",
    """\|SourceZone=({src_network_zone}[^\|]+?)\|""",
    """\|DestinationZone=({dest_network_zone}[^\|]+?)\|""",
    
}
```