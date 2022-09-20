#### Parser Content
```Java
{
Name = microsoft-defenderatp-sk4-alert-trigger-success-windowsdefenderav
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Defender ATP
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"ProviderName":"MDATP"""", """"VendorName":"Microsoft"""", """"AlertType":"WindowsDefenderAv"""" ]
  Fields=[
    """"HostName":\s*"((?i)localhost|({dest_host}[^"]+))""",
    """"TimeGenerated"+:"+({time}[^"]+)""",
    """"MicrosoftDefenderAtp.Category":\s*"({alert_type}[^"]+)""",
    """"AlertName"+:"+({alert_name}[^"]+)""",
    """"AlertSeverity"+:"+({alert_severity}[^"]+)""",
    """"SystemAlertId"+:"+({alert_id}[^"]+)""",
    """"AlertLink":\s*"({additional_info}[^"]+)""",
    """"LastIpAddress":\s*"({src_ip}[a-fA-F\d.:]+)"""
  ]
  DupFields = ["dest_host->host"]


}
```