#### Parser Content
```Java
{
Name = vmware-carbonblack-mix-alert-trigger-success-threat
  Vendor = VMware
  Product = Carbon Black CES
  TimeFormat = "epoch"
  Conditions = [ """"threatInfo":""", """"indicators":""", """"summary":""", """"ruleName":""", """"incidentId":""", """"THREAT"""" ]
  Fields = [
    """eventTime"+:\s*({time}\d{13})""",
    """email"+:\s*"+(({email_address}[^@"]+@[^"]+)|((({domain}[^\"]+?)\\+)?({user}[^"]+)))"""",
    """deviceName"+:\s*"+([^\\"]+\\+)?({src_host}[^"]+)"""",
    """ruleName"+:\s*"+(Confer - )?({alert_name}[^"]+)"""",
    """type"+:\s*"+({alert_type}[^"]+)"""",
    """incidentId"+:\s*"+({alert_id}[^"]+)"""",
    """score"+:\s*({alert_severity}\d+)""",
    """summary"+:\s*"+({additional_info}[^"]+)"""",
    """eventDescription"+:\s*"+({additional_info}[^"]+)"""",
    """deviceType"+:\s*"+({os}[^"]+)"""",
    """externalIpAddress"+:\s*"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """applicationName":\s"({process_name}[^"]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```