#### Parser Content
```Java
{
Name = cisco-securenwanalytics-kv-alert-trigger-success-additionalinfo
    Vendor = Cisco
    Product = Secure Network Analytics
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [ """|dest_host""", """|additional_info""", """|dest_ip""" ]
    Fields = [
      """time=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\w)""",
      """\|dest_host=(|({dest_host}.+?))\|""",
      """\|additional_info=({additional_info}[^\.\|]+)""",
      """\|dest_port=(|({dest_port}\d+))\|""",
      """\|dest_ip=({dest_ip}[a-fA-F\d.:]+)""",
      """\|dest_mac=(|({dest_mac}[^\|]+))\|""",
      """\|alert_name=(|({alert_name}[^\|]+))\|""",
      """\|alert_type=(|({alert_type}[^\|]+))\|""",
      """\|src_host=(|({src_host}[^\|]+))\|""",
      """\|alert_severity=({alert_severity}\d+)\|""",
      """\|src_ip=({src_ip}[a-fA-F\d.:]+)""",
      """\|src_mac=({src_mac}[a-fA-F\d.:]+)""",
      """\|user=(|({user}[^\|]+))\|""",
      """\|host_ip=({host_ip}[a-fA-F\d.:]+)""",
      """\|host=({host}[^\|]+)""",
      """\|protocol=(|({protocol}[^\|]+))\|""",
      """\|alert_id=({alert_id}[^\|]+?)(\||\s*$)""",
    ]
	ParserVersion = "v1.0.0"
  

}
```