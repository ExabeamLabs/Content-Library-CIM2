#### Parser Content
```Java
{
Name = microsoft-defenderep-json-network-notification-success-networkinfo
  ParserVersion = "v1.0.0"
  Product = "Microsoft Defender for Endpoint"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [""""Type":"AdvancedHuntingDeviceNetworkInfo_CL""", """IPAddresses_s""", """TenantId""", """TimeGenerated"""]
  Fields = ${DLMicrosoftParsersTemplates.defender-atp-events.Fields} [
     """TimeGenerated"*:"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
     """Computer"*:"*({host}[^"]+)""",
     """DeviceId_s"+:"+({device_id}[^"]+)"""",
     """IPAddress\\"+:\\"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
     """MacAddress_s"+:"+({src_mac}[^"]+)"""",
     """Type"+:"+({event_name}[^"]+)""",
  ]

defender-atp-events = {
    Vendor = Microsoft
    Product = Microsoft Defender for Endpoint
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
    Fields = [
      """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
      """"DeviceName":"({host}[^"]+)""""
      """"LogonType":"({login_type_text}[^"]+)"""",
      """"AccountName":"({user}[^"]+)"""",
      """"AccountDomain":"({domain}[^"]+)"""",
      """"InitiatingProcessFileName":"({process_name}[^"]+)"""",
      """"category":"({event_name}[^"]+)"""",
      """"ActionType":"({result}[^"]+)"""",
      """"RemoteIP":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
      """"Protocol":"({protocol}[^"]+)"""",
      """LogonId":(null|({login_id}[^:]+?)),""",
      """InitiatingProcessFolderPath":"({process_path}[^"]+?)",""",
      """InitiatingProcessFileName":"({process_name}[^:]+?)",""",
      """InitiatingProcessCommandLine":"({process_command_line}[^<]+?)\s*","InitiatingProcess""",
      """InitiatingProcessId":({process_id}[^:]+?),""",
      """DeviceId":"({device_id}[^:]+?)",""",
      """InitiatingProcessMD5":"({hash_md5}[^:]+?)","""
    ]
    DupFields = ["host->dest_host"
}
```