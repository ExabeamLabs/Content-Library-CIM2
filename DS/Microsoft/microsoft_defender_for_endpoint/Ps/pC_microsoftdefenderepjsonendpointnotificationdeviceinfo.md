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
     """PublicIP_s"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """UserName\\"+:\\"+({user}[^"]+)\\""",
     """DomainName\\"+:\\"+({domain}[^"]+)\\""",
     """DeviceName_s"+:\s*"+({src_host}[^"]+)""",
     """Type"+:"+({event_name}[^"]+)""",
     """DeviceId_s":"({device_id}[^"]+)"""",
  ]


}
```