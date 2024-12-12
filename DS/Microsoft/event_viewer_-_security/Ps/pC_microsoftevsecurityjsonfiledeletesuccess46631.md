#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-file-delete-success-4663-1
  Conditions = [ """"EVENT_NUMBER":"4663"""", """"REMARKS":"An object was deleted."""" ]
  Fields = ${ADAuditParserTemplates.ad-audit-json-events.Fields}[
    """exa_json_path=$.WORKSTATION_NAME,exa_field_name=src_host_windows,exa_match_expr=!InList($.WORKSTATION_NAME,"-")""",
    """exa_json_path=$.CLIENT_HOST_NAME,exa_regex=^(-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-.]+))$""",
    """exa_json_path=$.CLIENT_IP_ADDRESS,exa_regex=^({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?$""",
    """exa_json_path=$.SOURCE,exa_regex=^(-|({src_host}[\w\-.]+))$""",
    """exa_json_path=$.OBJECT_NAME,exa_regex=^({file_path}({file_dir}[^"]+)\\+({file_name}[^"]+))$""",
    """exa_json_path=$.FILE_NAME,exa_regex=^({file_name}[^"]+?(\.({file_ext}[^\."]+))?)$""",
    """exa_json_path=$.ACCESSES,exa_field_name=access""",
    """exa_json_path=$.ACCESS_MASK,exa_field_name=access_mask""",
    """exa_json_path=$.PROCESS_NAME,exa_field_name=process_path,exa_match_expr=!InList($.PROCESS_NAME,"")""",
    """exa_json_path=$.PROCESS_ID,exa_field_name=process_id"""
  ]
  ParserVersion = "v1.0.0"

ad-audit-json-events = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "epoch_sec"
  ExtractionType = json
  Fields = [
    """exa_json_path=$.TIME_GENERATED,exa_field_name=time""",
    """exa_json_path=$.CALLER_USER_NAME,exa_regex=^(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))$""",
    """exa_json_path=$.USERNAME,exa_regex=^({user}[\w\.\-\!\#\^\~]{1,40}\$?)$""",
    """exa_json_path=$.LOGON_TYPE,exa_field_name=login_type""",
    """exa_json_path=$.REMARKS,exa_field_name=event_name""",
    """exa_json_path=$.EVENT_NUMBER,exa_field_name=event_code""",
    """exa_json_path=$.DOMAIN,exa_field_name=domain""",
    """exa_json_path=$.CLIENT_PORT,exa_field_name=src_port""",
    """exa_json_path=$.SOURCE_PORT,exa_field_name=src_port""",
    """exa_json_path=$.LOGON_ID,exa_field_name=login_id""",
    """exa_json_path=$.USER_SID,exa_field_name=user_sid""",
    """exa_json_path=$.ERROR_CODE,exa_field_name=result_code,exa_match_expr=!InList($.ERROR_CODE,"null")""",
    """exa_json_path=$.EVENT_TYPE_TEXT,exa_field_name=result"""
  
}
```