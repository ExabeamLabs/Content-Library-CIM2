#### Parser Content
```Java
{
Name = forcepoint-dlp-cef-alert-trigger-success-tritonapdata
  ParserVersion = v1.0.0
  Vendor = Forcepoint
  Product = Forcepoint DLP
  TimeFormat = "epoch"
  Conditions = [ "|Forcepoint|TRITON AP-DATA", "sourceServiceName =" ]
  Fields = [
    """\srt=({time}\d+)""",
    """\sdvc=({host}[\d.]+)""",
    """\sdvchost=({host}[^\s]*)""",
    """\ssuser=({full_name}.+?)(\s+\(.+\))?\s\w+=""",
    """loginName =(({domain}[^\\]+)[\\]+)?({user}[^,=]+)\s+([\w\.]+=|$)""",
    """sourceIp=(?:N\/A|({src_ip}.+?))\s+([\w\.]+=|$)""",
    """sourceHost=({src_host}.+?)\s+([\w\.]+=|$)""",
    """\sduser=({url}(\w+:\/+)?({web_domain}[^\\\/\s]+)[^\s]+)\s\w+=""",
    """\sfname=(N\/A|.*?[\/\\]*({file_name}[^\\\/]+))\s+\- [\d.]+ """,
    """\sfname=(N\/A|.*? - ({bytes}\d+)\s+({bytes_unit}[^\s;]+))""",
    """\ssourceServiceName =({alert_type}.+?)\s+(on |\w+=)""",
    """\scat=\*({alert_name}.+?)(\*|\s\-\s|\s+[\w\.]+=)""",
    """\|Forcepoint\|([^|]+?\|){4}({alert_severity}[^|]+)""",
    """\sact=({action}[^\s]*)"""
  ]


}
```