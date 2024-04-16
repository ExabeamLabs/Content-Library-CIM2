#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-share-access-success-5140-3
    Vendor = Microsoft
    Product = "Event Viewer - Security"
    ParserVersion = v1.0.0
    TimeFormat = "yyyy-dd-MM'T'HH:mm:ss.SSSZ"
    ExtractionType = json
    Conditions = ["""A network share object was accessed""", """"SubjectUserName":""", """"event_id":"5140""",""""Microsoft-Windows-Security-Auditing"""",""""ShareName":""""]
    Fields = [
      """exa_json_path=$.message,exa_regex=({event_name}A network share object was accessed)""",
      """exa_json_path=$..created,exa_field_name=time""",
      """exa_json_path=$..event_id,exa_field_name=event_code""",
      """exa_json_path=$..SubjectLogonId,exa_field_name=login_id""",
      """exa_json_path=$..AccessList,exa_field_name=access""",
      """exa_json_path=$.message,exa_regex=Accesses:\s*({access}.*?)(\s|\\[nrt])+"*$""",
      """exa_json_path=$..SubjectUserName,exa_regex=^({user}[\w\.\-]{1,40}\$?)$""",
      """exa_json_path=$..SubjectDomainName,exa_field_name=domain""",
      """exa_json_path=$..IpAddress,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$""",
      """exa_json_path=$..ShareName,exa_regex=^([\\*]+)?({share_name}[^"]+)$""",
      """exa_json_path=$..outcome,exa_field_name=result""",
      """exa_json_path=$.host,exa_regex=^({host}[\w.\-]+)$""",
      """exa_json_path=$.message,exa_regex=Logon ID:\s({login_id}[^\s]+)""",
      """exa_json_path=$..IpPort,exa_field_name=src_port""",
      """exa_json_path=$..SubjectUserSid,exa_field_name=user_sid""",
      """exa_json_path=$..action,exa_field_name=operation"""
    ]
    DupFields=[ "host->dest_host" ]


}
```