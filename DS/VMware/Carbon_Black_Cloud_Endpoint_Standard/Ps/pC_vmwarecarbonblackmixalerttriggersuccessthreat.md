#### Parser Content
```Java
{
Name = vmware-carbonblack-mix-alert-trigger-success-threat
  Vendor = VMware
  Product = Carbon Black Cloud Endpoint Standard
  TimeFormat = "epoch"
  Conditions = [ """"threatInfo":""", """"indicators":""", """"summary":""", """"ruleName":""", """"incidentId":""", """"THREAT"""" ]
  Fields = [
    """eventTime"+:\s*({time}\d+)""",
    """email"+:\s*"+(({email_address}[^@"]+@[^"]+)|((({domain}[^\"]+)\+)?({user}[^"]+)))"""",
    """deviceName"+:\s*"+([^\"]+\+)?({src_host}[^"]+)"""",
    """ruleName"+:\s*"+(Confer - )?({alert_name}[^"]+)"""",
    """type"+:\s*"+({alert_type}[^"]+)"""",
    """incidentId"+:\s*"+({alert_id}[^"]+)"""",
    """score"+:\s*({alert_severity}\d+)""",
    """summary"+:\s*"+({additional_info}[^"]+)"""",
    """eventDescription"+:\s*"+({additional_info}[^"]+)"""",
    """deviceType"+:\s*"+({os}[^"]+)"""",
    """externalIpAddress"+:\s*"+({dest_ip}[^"]+)"""",
    """applicationName":\s"({process_name}[^"]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```