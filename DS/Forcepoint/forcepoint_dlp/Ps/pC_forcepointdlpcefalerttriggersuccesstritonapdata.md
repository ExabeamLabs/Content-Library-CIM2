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
    """\srt=({time}\d{13})""",
    """\sdvc=({host}[\d.]+)""",
    """\sdvchost=({host}[^\s]*)""",
    """\ssuser=({full_name}.+?)(\s+\(.+\))?\s\w+=""",
    """sourceIp=(?:N\/A|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s+([\w\.]+=|$)""",
    """sourceHost=({src_host}.+?)\s+([\w\.]+=|$)""",
    """\sduser=({url}(\w+:\/+)?({web_domain}[^\\\/\s]+)[^\s]+)\s\w+=""",
    """loginName =(({domain}[^\\]+)[\\]+)?({user}[^,=]+)\s+([\w\.]+=|$)""",
    """\sfname=(N\/A|.*?[\/\\]*({file_name}[^\\\/]+))\s+\- [\d.]+ """,
    """\sfname=(N\/A|.*? - ({bytes}\d+)\s+({bytes_unit}[^\s;]+))""",
    """\ssourceServiceName =({alert_type}.+?)\s+(on |\w+=)""",
    """\scat=\**({alert_name}.+?)(\*|\s\-\s|\s+[\w\.]+=)""",
    """\|Forcepoint\|([^|]+?\|){4}({alert_severity}[^|]+)""",
    """\sact=({action}[^\s]*)"""
  ]


}
```