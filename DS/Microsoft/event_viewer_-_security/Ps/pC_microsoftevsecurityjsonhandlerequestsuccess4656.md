#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-handle-request-success-4656
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ParserVersion = v1.0.0
  ExtractionType = json
  Conditions = [ """"data.id":"4656"""", """"type":"wazuh-alerts""""  , """"decoder.parent":"windows""""  ]
  Fields = [
    """exa_json_path=$.['data.id'],exa_field_name=event_code""",
    """exa_json_path=$.@timestamp,exa_field_name=time""",
    """exa_json_path=$.['data.dstuser'],exa_regex=(\(no user\)|({dest_user}[\w\.\-]{1,40}\$?))""",
    """exa_json_path=$.['data.status'],exa_field_name=result""",
    """exa_json_path=$.location,exa_field_name=log_location""",
    """exa_json_path=$.['data.data'],exa_field_name=data""",
    """exa_json_path=$.path,exa_field_name=log_path""",
    """exa_json_path=$.['data.system_name'],exa_regex=^({host}[\w\-.]+)$""",
    """exa_json_path=$.['agent.id'],exa_field_name=agent_id""",
    """exa_json_path=$.['manager.name'],exa_field_name=wazuh_manager""",
    """exa_json_path=$.['rule.description'],exa_field_name=description""",
    """exa_json_path=$.['decoder.name'],exa_field_name=decoder_name""",
    """exa_json_path=$.full_log,exa_regex=({event_name}A handle to an object was ({operation_type}requested))""",
    """exa_json_path=$.['data.subject.security_id'],exa_field_name=user_sid""",
    """exa_json_path=$.['data.subject.account_name'],exa_regex=^({user}[\w\.\-]{1,40}\$?)$""",
    """exa_json_path=$.['data.subject.account_domain'],exa_field_name=domain""",
    """exa_json_path=$.['data.subject.logon_id'],exa_field_name=login_id""",
    """exa_json_path=$.full_log,exa_regex=Object Server:\s*({object_server}\S.*?)\s+Object Type:""",
    """exa_json_path=$.full_log,exa_regex=Object Type:\s*({object_class}.+?)\s*Object Name:""",
    """exa_json_path=$.full_log,exa_regex=Object Name:\s*({object}\S.*?)\s*Handle ID:""",
    """exa_json_path=$.full_log,exa_regex=Process ID:\s*({process_id}[^\s]*)""",
    """exa_json_path=$.full_log,exa_regex=Process Name:\s*({process_path}({process_dir}.+)[\\\/]({process_name}.+?))\s*Access Request Information:""",
    """exa_json_path=$.full_log,exa_regex=Transaction ID:\s*({transaction_id}[^\s]+)\s*Accesses:""",
    """exa_json_path=$.['data.accesses'],exa_field_name=access""",
    """exa_json_path=$.full_log,exa_regex=Accesses:\s*({access}\S.*?)\s*Access Reasons:""",
    """exa_json_path=$.full_log,exa_regex=Access Reasons:\s*(-|({access}\S.*?))\s*Access Mask:""",
    """exa_json_path=$.full_log,exa_regex=Privileges Used for Access Check:\s*(-|({privileges}.*?))\s*Restricted SID Count:""",
    """exa_json_path=$.full_log,exa_regex=Handle ID:\s*({object_id}.+?)\s"""
  ]


}
```