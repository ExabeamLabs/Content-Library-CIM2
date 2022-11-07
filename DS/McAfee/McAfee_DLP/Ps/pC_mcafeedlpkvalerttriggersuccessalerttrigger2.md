#### Parser Content
```Java
{
Name = mcafee-dlp-kv-alert-trigger-success-alerttrigger-2
  ParserVersion = v1.0.0
  Vendor = McAfee
  Product = McAfee DLP
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = ["""Occured_(Endpoint)="""" , """ Device_Class_Name ="""" , """ Policy_Rule="""" , """Incident_Type=""""]
  Fields = [
    """Occured_\(Endpoint\)="({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)""",
    """Incident_ID="({alert_id}[^"]+)"""",
    """Severity="({alert_severity}[^"]+)"""",
    """Policy_Rule="({alert_name}[^"]+)"""",
    """Computer_Name ="({host}[^"]+)"""",
    """Domain_Account="(({domain}[^\\]+)\\)?({user}[^"]+)"""",
    """Incident_Type="({alert_type}[^"]+)"""",
    """Device_Friendly_Name ="({device_id}[^"]+)"""",
    """Actual_Action="({action}[^"]+)"""",
    """Domain_Account_OU="({additional_info}[^"]+)"""",
    """Computer_IP="({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""""
  ]


}
```