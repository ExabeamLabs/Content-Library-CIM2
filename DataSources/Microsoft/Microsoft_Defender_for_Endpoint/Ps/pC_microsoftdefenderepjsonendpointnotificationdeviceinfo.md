#### Parser Content
```Java
{
Name = microsoft-defenderep-json-endpoint-notification-deviceinfo
  Vendor = Microsoft
  ParserVersion = "v1.0.0"
  Product = "Microsoft Defender for Endpoint"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [""""AdvancedHunting-DeviceInfo"""" , """TenantId""", """TimeGenerated"""]
  Fields = [
     """TimeGenerated"*:"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
     """Computer"*:"*({host}[^"]+)""",
     """OSPlatform_s"+:"+({os}[^",]+)""",
     """PublicIP_s"+:"+({src_ip}[A-Fa-f:\d.]+)""",
     """UserName\\"+:\\"+({user}[^"]+)\\""",
     """DomainName\\"+:\\"+({domain}[^"]+)\\""",
     """DeviceName_s"+:\s*"+({src_host}[^"]+)""",
     """Type"+:"+({event_name}[^"]+)""",
     """DeviceId_s":"({device_id}[^"]+)"""",
  ]


}
```