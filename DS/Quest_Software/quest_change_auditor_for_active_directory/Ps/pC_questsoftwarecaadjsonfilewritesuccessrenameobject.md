#### Parser Content
```Java
{
Name = "questsoftware-caad-json-file-write-success-renameobject"
  Conditions = [
  """"action": "Rename Object""""
  """"folderPath": """"
  """"timeDetected": """"
  ]
  ParserVersion = "v1.0.0"

quest-caad-json-file-events = {
    Vendor = Quest Software
    Product = Quest Change Auditor for Active Directory
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    ExtractionType = json
    Fields = [
      """exa_json_path=$.timeDetected,exa_field_name=time""",
      """exa_json_path=$.severity,exa_field_name=alert_severity""",
      """exa_json_path=$.result,exa_field_name=result""",
      """exa_json_path=$.event,exa_field_name=action""",
      """exa_json_path=$.user,exa_regex=^({user}[\w\.\-\!\#\^\~]{1,40}\$?)$""",
      """exa_json_path=$.userMail,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
      """exa_json_path=$.userSid,exa_field_name=user_sid""",
      """exa_json_path=$.originIPv4,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """exa_json_path=$.computer,exa_field_name=dest_host""",
      """exa_json_path=$.domain,exa_field_name=domain""",
      """exa_json_path=$.folderPath,exa_field_name=file_path""",
      """exa_json_path=$.fileName,exa_regex=({file_name}[^"]+?(\.({file_ext}[^"\.]+))?)$""",
      """exa_json_path=$.description,exa_field_name=additional_info""",
      """exa_json_path=$.event,exa_regex=(EMC )?(File|Folder) ({access}(opened|deleted|moved|renamed|created|contents written))""",
      """exa_json_path=$.action,exa_regex=({access}(Delete|Move|Rename|Add)) Object"""
    ]
    DupFields = [
    "file_path->file_dir"
    
}
```