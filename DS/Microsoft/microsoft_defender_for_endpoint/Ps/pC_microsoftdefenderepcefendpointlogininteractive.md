#### Parser Content
```Java
{
Name = microsoft-defenderep-cef-endpoint-login-interactive
  ParserVersion = v1.0.0
  Conditions = [ """DeviceLogonEvents""", """"LogonType":"Interactive"""", """"InitiatingProcessParentFileName":""" ]

cef-defender-atp-events = {
    Vendor = Microsoft
    Product = Microsoft Defender for Endpoint
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
    Fields = [
      """"(time|TimeGenerated)":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
      """"DeviceName":"({host}[\w\-.]+)""""
      """"LogonType":"({login_type_text}[^"]+)"""",
      """"AccountName":"(({full_name}[^"\s]+\s[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
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
      """exa_regex="(time|TimeGenerated)":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
      """exa_json_path=$..DeviceName,exa_field_name=host"""
      """exa_json_path=$.DeviceName,exa_field_name=host"""
      """exa_json_path=$..LogonType,exa_field_name=login_type_text"""
      """exa_json_path=$.LogonType,exa_field_name=login_type_text"""
      """exa_json_path=$..AccountName,exa_regex=(({full_name}[^"\s]+\s[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
      """exa_json_path=$.AccountName,exa_regex=(({full_name}[^"\s]+\s[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
      """exa_json_path=$..AccountDomain,exa_field_name=domain"""
      """exa_json_path=$.AccountDomain,exa_field_name=domain"""
      """exa_json_path=$..InitiatingProcessFileName,exa_field_name=process_name"""
      """exa_json_path=$.InitiatingProcessFileName,exa_field_name=process_name"""
      """exa_json_path=$.category,exa_field_name=event_name"""
      """exa_json_path=$..ActionType,exa_field_name=result"""
      """exa_json_path=$.ActionType,exa_field_name=result"""
      """exa_json_path=$..Protocol,exa_field_name=protocol"""
      """exa_json_path=$.Protocol,exa_field_name=protocol"""
      """exa_json_path=$.LogonId,exa_regex=(null|({login_id}[^",]+))"""
      """exa_json_path=$..LogonId,exa_regex=(null|({login_id}[^",]+))"""
      """exa_json_path=$..InitiatingProcessFolderPath,exa_field_name=process_path"""
      """exa_json_path=$.InitiatingProcessFolderPath,exa_field_name=process_path"""
      """exa_json_path=$..InitiatingProcessCommandLine,exa_field_name=process_command_line"""
      """exa_json_path=$.InitiatingProcessCommandLine,exa_field_name=process_command_line"""
      """exa_json_path=$..InitiatingProcessId,exa_field_name=process_id"""
      """exa_json_path=$.InitiatingProcessId,exa_field_name=process_id"""
      """exa_json_path=$..InitiatingProcessMD5,exa_field_name=hash_md5"""
      """exa_json_path=$.InitiatingProcessMD5,exa_field_name=hash_md5"""
      """exa_json_path=$..FailureReason,exa_field_name=failure_reason"""
      """exa_json_path=$.FailureReason,exa_field_name=failure_reason"""
      """exa_json_path=$..InitiatingProcessAccountName,exa_field_name=account"""
      """exa_json_path=$.InitiatingProcessAccountName,exa_field_name=account"""
      """exa_json_path=$.DeviceId,exa_field_name=device_id"""
      """exa_json_path=$..DeviceId,exa_field_name=device_id"""
    ]
    DupFields = ["host->dest_host"
}
```