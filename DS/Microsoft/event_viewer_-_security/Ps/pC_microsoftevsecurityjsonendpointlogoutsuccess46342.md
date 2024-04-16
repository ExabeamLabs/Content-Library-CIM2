#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-logout-success-4634-2
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  ExtractionType = json
  Conditions = [ """"data.id":"4634"""", """"type":"wazuh-alerts""""  , """"decoder.parent":"windows"""" ]
  Fields = [
    """exa_json_path=$.['data.id'],exa_field_name=event_code""",
    """exa_json_path=$.@timestamp,exa_field_name=time""",
    """exa_json_path=$.['data.dstuser'],exa_regex=^(\(no user\)|({dest_user}[^"]+))$""",
    """exa_json_path=$.['data.status'],exa_field_name=result""",
    """exa_json_path=$.location,exa_field_name=log_location""",
    """exa_json_path=$.['data.data'],exa_field_name=data""",
    """exa_json_path=$.path,exa_field_name=log_path""",
    """exa_json_path=$.['data.system_name'],exa_regex=^({host}[\w\-.]+)$""",
    """exa_json_path=$.['agent.id'],exa_field_name=agent_id""",
    """exa_json_path=$.['manager.name'],exa_field_name=wazuh_manager""",
    """exa_json_path=$.['rule.description'],exa_field_name=description""",
    """exa_json_path=$.['decoder.name'],exa_field_name=decoder_name""",
    """exa_json_path=$.full_log,exa_regex=({event_name}An account was logged off)"""
    """exa_json_path=$.['data.subject.security_id'],exa_field_name=user_sid""",
    """exa_json_path=$.['data.subject.account_name'],exa_regex=^({user}[\w\.\-]{1,40}\$?)$""",
    """exa_json_path=$.['data.subject.account_domain'],exa_field_name=domain""",
    """exa_json_path=$.['data.subject.logon_id'],exa_field_name=login_id""",
    """exa_json_path=$.['data.logon_type'],exa_field_name=login_type"""
  ]


}
```