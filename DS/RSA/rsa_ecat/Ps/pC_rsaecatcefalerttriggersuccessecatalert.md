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
    """\ssrc=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sfname=({process_name}.+?)\s+(\w+=|$)""",
    """\sinstantIOCName =({alert_name}.+?)\s+(\w+=|$)""",
    """\smachineScore=({alert_severity}\d+)""",
    """\smoduleSignature=({additional_info}.+?)\s+(\w+=|$)""",
    """\sos=({threat_category}.+?)\s+(\w+=|$)""",
    """\stargetModule=({malware_url}.+?)\s+(\w+=|$)""",
  ]
  DupFields = [ "dest_host->host" , "malware_url->process_name"]
  ParserVersion = "v1.0.0"


}
```