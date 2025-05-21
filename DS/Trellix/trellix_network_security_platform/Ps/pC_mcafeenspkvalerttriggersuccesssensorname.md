#### Parser Content
```Java
{
Name = mcafee-nsp-kv-alert-trigger-success-sensorname
  Vendor = Trellix
  Product = Trellix Network Security Platform
  TimeFormat = "yyyy-MM-dd HH:mm:ss z"
  Conditions = [ """SyslogAlertForwarder:""", """Attack Name:""", """Sensor Name:""" ]
  Fields = [
    """\WAttack ID:\s*({attack_id}[^;\s]+);""",
    """\WAttack Name:\s*({alert_name}[^;]+);""",
    """\WResult Status:\s*(?:n\/a|({result}[^;]+));""",
    """\WAdmin Domain:\s*({domain}[^;]+);""",
    """\WSensor Name:\s*({sensor}[^;]+);""",
    """\WAttack Time:\s*({time}\d+\-\d+\-\d+ \d+:\d+:\d+ \w+)""",
    """\WInterface:\s*({interface}[^;]+);""",
    """\WDirection:\s*({direction}[^;]+);""",
    """Direction:\s*Outbound;.*?SIP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}));\s*SPort:\s*(?:N/A|({src_port}\d+));\s*DIP:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}));\s*DPort:\s*(?:N/A|({dest_port}\d+));""",
    """Direction:\s*Inbound;.*?SIP:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}));\s*SPort:\s*(?:N/A|({dest_port}\d+));\s*DIP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}));\s*DPort:\s*(?:N/A|({src_port}\d+));""",
    """\WApp Proto:\s*(?:N/A|({app_protocol}[^;]+));""",
    """\WNet Proto:\s*({protocol}[^;]+);""",
    """\WAlert ID:\s*({alert_id}\d+)""",
    """\WAlert Type:\s*({alert_type}[^;]+);""",
    """\WAttack Severity:\s*({alert_severity}[^;]+);""",
    """\WAttack Conf:\s*({attack_conf}[^;]+);""",
    """\WCat:\s*({category}[^;]+);""",
    """\WSub-Cat:\s*({sub_category}[^;]+);""",
    """\WDetection Mech:\s*({detection_mech}[^;]+);"""
  ]
  ParserVersion = "v1.0.0"


}
```