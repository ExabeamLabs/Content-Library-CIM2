#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-success-540"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
ExtractionType = json
Conditions = [ """"event_id":540,""", """Successful Network Logon:""" ]
Fields = [
  """exa_json_path=$.message,exa_regex=({event_name}Successful Network Logon)""",
  """exa_json_path=$.@timestamp,exa_field_name=time""",
  """exa_json_path=$.computer_name,exa_regex=^({host}[\w\-.]+?)$""",
  """exa_json_path=$.event_id,exa_field_name=event_code""",
  """exa_json_path=$.user.domain,exa_field_name=domain""",
  """exa_json_path=$.user.name,exa_regex=^({user}[\w\.\-\!\#\^\~]{1,40}\$?)$""",
  """exa_json_path=$..param1,exa_regex=^({user}[\w\.\-\!\#\^\~]{1,40}\$?)$""",
  """exa_json_path=$..UserName,exa_regex=^({user}[\w\.\-\!\#\^\~]{1,40}\$?)$""",
  """exa_json_path=$..param2,exa_field_name=domain""",
  """exa_json_path=$..Domain,exa_field_name=domain""",
  """exa_json_path=$..param14,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """exa_json_path=$..SourceNetworkAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """exa_json_path=$..source_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """exa_json_path=$..param7,exa_field_name=src_host_windows""",
  """exa_json_path=$..Workstation,exa_field_name=src_host_windows""",
  """exa_json_path=$..workstation_name,exa_field_name=src_host_windows""",
  """exa_json_path=$..param5,exa_regex=^({auth_process}[^"]+?)\s*$""",
  """exa_json_path=$..LogonProcess,exa_regex=^({auth_process}[^"]+?)\s*$""",
  """exa_json_path=$..param6,exa_field_name=auth_package""",
  """exa_json_path=$..AuthenticationPackage,exa_field_name=auth_package""",
  """exa_json_path=$..authentication_package,exa_field_name=auth_package""",
  """exa_json_path=$..param3,exa_regex=^\(([\dxA-F]+,)?({login_id}.+?)\)$""",
  """exa_json_path=$..LogonId,exa_regex=^\(([\dxA-F]+,)?({login_id}.+?)\)$""",
  """exa_json_path=$..logon_id,exa_regex=^\(([\dxA-F]+,)?({login_id}.+?)\)$""",
  """exa_json_path=$..param4,exa_field_name=login_type""",
  """exa_json_path=$..LogonType,exa_field_name=login_type"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```