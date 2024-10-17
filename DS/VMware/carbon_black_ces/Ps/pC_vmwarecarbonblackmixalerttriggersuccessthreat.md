#### Parser Content
```Java
{
Name = vmware-carbonblack-mix-alert-trigger-success-threat
  Vendor = VMware
  Product = Carbon Black CES
  TimeFormat = "epoch"
  ExtractionType = json
  Conditions = [ """"threatInfo":""", """"indicators":""", """"summary":""", """"ruleName":""", """"incidentId":""", """"THREAT"""" ]
  Fields = [
    """eventTime"+:\s*({time}\d{13})""",
    """email"+:\s*"+(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|((({domain}[^\"]+?)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""",
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

    """exa_json_path=$.eventTime,exa_field_name=time""",
    """exa_json_path=$.deviceInfo.email,exa_regex=^(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|((({domain}[^\"]+?)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))$""",
    """exa_json_path=$.deviceInfo.deviceName,exa_regex=^([^\\"]+\\+)?({src_host}[\w\-.]+)$""",
    """exa_json_path=$.deviceInfo.deviceType,exa_field_name=os""",
    """exa_json_path=$.deviceInfo.externalIpAddress,exa_regex=^({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?$""",
    """exa_json_path=$.ruleName,exa_regex=^(Confer - )?({alert_name}[^"]+)$""",
    """exa_json_path=$.type,exa_field_name=alert_type""",
    """exa_json_path=$.threatInfo.incidentId,exa_field_name=alert_id""",
    """exa_json_path=$.threatInfo.score,exa_field_name=alert_severity""",
    """exa_json_path=$.threatInfo.summary,exa_field_name=additional_info""",
    """exa_json_path=$.eventDescription,exa_field_name=additional_info""",
    """exa_json_path=$.threatInfo.indicators[0].applicationName,exa_field_name=process_name"""
  ]
  ParserVersion = "v1.0.0"


}
```