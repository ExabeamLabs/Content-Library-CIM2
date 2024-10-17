#### Parser Content
```Java
{
Name = symantec-dlp-str-alert-trigger-success-symcdlpsys
  Vendor = Symantec
  Product = Symantec DLP
  Conditions = [ """|symcdlpsys|""","""|POLICY|""", """|MONITOR_NAME|""", """|APPLICATION_NAME|""" ]
  TimeFormat = "MMM dd, yyyy HH:mm:ss a"
  Fields = [
    """OCCURRED_ON\|({time}\w+\s+\d{1,2},\s*\d{1,4}\s+\d{1,2}:\d{1,2}:\d{1,2}\s+(AM|PM|am|pm))""",
    """:\d\d\s+({host}[^\s]+)\s\|symcdlpsys""",
    """\|\s*INCIDENT_ID\|({alert_id}\d+)\|""",
    """\|\s*POLICY\|({alert_name}[^\|]+)\|""",
    """\|\s*SEVERITY\|({alert_severity}[^\|]+)\|""",
    """\|\s*PROTOCOL\|({protocol}[^\|]+)\|""",
    """\|\s*BLOCKED\|(None|({action}\w+))\|""",
    """\|\s*ENDPOINT_USERNAME\|(N\/A|(({domain}[^\s\\\|@]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\|""",
    """\|\s*TARGET\|(N\/A|({target}[^\|]+))\|""",
    """\|\s*APPLICATION_NAME\|(N\/A|({additional_info}[^\|]+))\|""",
    """\|\s*RULES\|({alert_type}[^\|]+)\|""",
    """\|\s*SENDER\|(N\/A|({email_address}([^\|]+)@({email_domain}[^\|]+)))""",
    """\|\s*MACHINE_IP\|({src_ip}[a-fA-F\d\.:]+)\|""",
    ]
    ParserVersion = "v1.0.0"


}
```