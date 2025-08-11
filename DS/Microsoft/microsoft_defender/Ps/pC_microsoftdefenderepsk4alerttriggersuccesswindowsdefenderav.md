#### Parser Content
```Java
{
Name = microsoft-defenderep-sk4-alert-trigger-success-windowsdefenderav
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Microsoft Defender
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"ProviderName":"MDATP"""", """"VendorName":"Microsoft"""", """"AlertType":"WindowsDefenderAv"""" ]
  Fields=[
    """"HostName":\s*"((?i)localhost|({dest_host}[\w\-.]+))""",
    """"TimeGenerated"+:"+({time}[^"]+)""",
    """"MicrosoftDefenderAtp.Category":\s*"({alert_type}[^"]+)""",
    """"AlertName"+:"+({alert_name}[^"]+)""",
    """"AlertSeverity"+:"+({alert_severity}[^"]+)""",
    """"SystemAlertId"+:"+({alert_id}[^"]+)""",
    """"AlertLink":\s*"({additional_info}[^"]+)""",
    """"LastIpAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """"Status_string":"({incident_status}[^"]+)"""
    """"incidentId":\s*"({alert_id}\d+)"""
    """"mitreTechniques":\s*\[({technique}[^\]]+)\]"""
    """"evidence".+?"verdict":\s*"({result}[^"]+)"""
  ]
  DupFields = ["dest_host->host"]


}
```