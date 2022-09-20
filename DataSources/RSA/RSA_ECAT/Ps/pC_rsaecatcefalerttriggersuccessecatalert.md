#### Parser Content
```Java
{
Name = rsa-ecat-cef-alert-trigger-success-ecatalert
  Vendor = RSA
  Product = RSA ECAT
  TimeFormat = "M/d/yyyy HH:mm:ss a"
  Conditions = [ """|RSA|RSA ECAT|""", """|EcatAlert|""" ]
  Fields = [
    """CEF([^\|]*\|){4}({alert_type}[^\|]+)""",
    """\sshost=({dest_host}.+?)\s+(\w+=|$)""",
    """\ssrc=({dest_ip}[a-fA-F\d.:]+)""",
    """\sfname=({process_name}.+?)\s+(\w+=|$)""",
    """\sinstantIOCName =({alert_name}.+?)\s+(\w+=|$)""",
    """\smachineScore=({alert_severity}\d+)""",
    """\smoduleSignature=({additional_info}.+?)\s+(\w+=|$)""",
    """\sos=({threat_category}.+?)\s+(\w+=|$)""",
    """\stargetModule=({url}.+?)\s+(\w+=|$)""",
  ]
  DupFields = [ "dest_host->host" , "url->process_name"]
  ParserVersion = "v1.0.0"


}
```