#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-alert-trigger-success-scenario
    Vendor = CrowdStrike
    Product = Falcon
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [ """"scenario":"""", """"detection_id":""", """"tactic":"""", """"technique":""""]
    Fields = [
      """"scenario":"({alert_name}[^"]+)""",
      """"technique":"({alert_type}[^"]+)""",
      """"severity":({alert_severity}\d+)""",
      """"detection_id":"({alert_id}[^"]+)""",
      """"user_name":"({user}[^"]+)""",
      """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
      """"md5":"(N\/A|({hash_md5}\w+))""",
      """"local_ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """"machine_domain":"({domain}[^"]+)""",
      """"filename":"({process_name}[^"]+)""",
      """"hostname":"({src_host}[^"]+)""",
      """"show_in_ui":.*?"status":"({action}[^"]+)""",
      """"cmdline":"({additional_info}.+?)\s*","""",
      """"tactic":"({category}[^"]+)""",
      """"((?i)SHA256|SHA256String|SHA256HashData)\\*"+:\s*\\*"+({hash_sha256}[^,]+?)\\*"+,""",
      """"(?i)Quarantine_File"+:\s*({quarantine_file}true|false)""",
      """"(?i)Quarantine_Machine"+:\s*({quarantine_machine}true|false)""",
      """"(?i)Detect"+:\s*({detect}true|false)""",
      """"(?i)Registry_Operation_Blocked"+:\s*({registry_operation_blocked}true|false)""",
      """"(?i)Kill_Parent"+:\s*({kill_parent}true|false)""",
      """"(?i)Operation_Blocked"+:\s*({operation_blocked}true|false)""",
      """"(?i)Kill_Process"+:\s*({kill_process}true|false)""",
      """"(?i)Process_Blocked"+:\s*({process_blocked}true|false)""",
      """"(?i)Policy_Disabled"+:\s*({policy_disabled}true|false)""",
      """"(?i)Sensor_Only"+:\s*({sensor_only}true|false)""",
      """"(?i)Kill_SubProcess"+:\s*({kill_sub_process}true|false)""",
      """"(?i)Rooting"+:\s*({rooting}true|false)""",
      """"(?i)Inddet_Mask"+:\s*({inddet_mask}true|false)""",
      """"(?i)Indicator"+:\s*({indicator}true|false)"""
    ]
    DupFields = [ "src_host->host" ]
 ParserVersion = "v1.0.0"


}
```