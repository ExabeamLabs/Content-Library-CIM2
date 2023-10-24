#### Parser Content
```Java
{
Name = microsoft-defenderep-json-endpoint-activity-registryevents
  ParserVersion = "v1.0.0"
  Product = "Microsoft Defender for Endpoint"
  Conditions = [  """"Type":"AdvancedHuntingDeviceRegistryEvents_CL""", """TenantId""", """TimeGenerated""", """ProcessAccountName_s""" ]
  Fields = ${DLMicrosoftParsersTemplates.defender-atp-events.Fields}[
     """ActionType_s":\s*"({action}[^"]+)""",
     """RegistryValueData_s":\s*"(|(\\")*({object}.+?))(\\"\s)?","[^\\"]+":(null|")""",
     """RegistryKey_s":\s*"(|({resource}[^"]+))""""

]

defender-atp-events = {
    Vendor = Microsoft
    Product = Microsoft Defender for Endpoint
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
    Fields = [
      """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
      """"DeviceName":"({host}[\w\-.]+)""""
      """"LogonType":"({login_type_text}[^"]+)"""",
      """"AccountName":"(({full_name}[^"\s]+\s[^"]+)|({user}[\w\.\-]{1,40}\$?))"""",
      """"AccountDomain":"({domain}[^"]+)"""",
      """"InitiatingProcessFileName":"({process_name}[^"]+)"""",
      """"category":"({event_name}[^"]+)"""",
      """"ActionType":"({result}[^"]+)"""",
      """"RemoteIP":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
      """"Protocol":"({protocol}[^"]+)"""",
      """LogonId":(null|({login_id}[^:]+?)),""",
      """InitiatingProcessFolderPath":"({process_path}[^"]+?)",""",
      """InitiatingProcessFileName":"({process_name}[^:]+?)",""",
      """InitiatingProcessCommandLine":"({process_command_line}[^<]+?)\s*","InitiatingProcess""",
      """InitiatingProcessId":({process_id}[^:]+?),""",
      """DeviceId":"({device_id}[^:]+?)",""",
      """InitiatingProcessMD5":"({hash_md5}[^:]+?)",""",
      """"FailureReason":"({failure_reason}[^"]+)"""",
      """"InitiatingProcessAccountName":"({account}[^"]+)""""
    ]
    DupFields = ["host->dest_host"
}
```