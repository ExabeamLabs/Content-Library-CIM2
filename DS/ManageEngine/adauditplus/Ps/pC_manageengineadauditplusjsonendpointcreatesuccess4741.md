#### Parser Content
```Java
{
Name = manageengine-adauditplus-json-endpoint-create-success-4741
  ParserVersion = "v1.0.0"
  Conditions = [ """"EVENT_NUMBER":"4741"""", """"A computer account was created."""" ]
  Fields = ${ADAuditParserTemplates.ad-audit-plus-json-events.Fields}[
    """exa_json_path=$.OBJECT_CLASS,exa_field_name=object_type"""
  ]

ad-audit-plus-json-events = {
  Vendor = ManageEngine
  Product = ADAuditPlus
  ExtractionType = json
  TimeFormat = "epoch"
  Fields = [
    """exa_json_path=$.TARGET0_ON_SID,exa_field_name=user_sid""",
    """exa_json_path=$.Category,exa_field_name=category""",
    """exa_json_path=$.TARGET0_OBJECT_ID,exa_field_name=object_id""",
    """exa_json_path=$.SOURCE,exa_regex=^(-|({src_host}[\w\-.]+))$""",
    """exa_json_path=$.ACTOR_IP_ADDRESS,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.ORIGIN,exa_field_name=origin_name""",
    """exa_json_path=$.ACTIVITY_TYPE,exa_field_name=operation_type""",
    """exa_json_path=$.TIME_GENERATED,exa_field_name=time""",
    """exa_json_path=$.TARGET0_UPN,exa_regex=(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_json_path=$.host,exa_field_name=host""",
    """exa_json_path=$.RECORD_ID,exa_field_name=event_id""",
    """exa_json_path=$.sourcetype,exa_field_name=protocol""",
    """exa_json_path=$.USER_MGMT_TYPE,exa_field_name=event_category""",
    """exa_json_path=$.ACTIVITY_RESULT_STATUS,exa_field_name=result""",
    """exa_json_path=$.CORRELATION_ID,exa_field_name=correlation_id""",
    """exa_json_path=$.ATTRIBUTES_TEXT,exa_field_name=attribute""",
    """exa_json_path=$.ACTIVITY_OPERATION_TYPE,exa_field_name=operation_type""",
    """exa_json_path=$.TARGET0_RES_TYPE,exa_field_name=resource_type""",
    """exa_json_path=$.REPORT_PROFILE,exa_field_name=action""",
    """exa_json_path=$.ACTOR_UPN,exa_field_name=user_upn""",
    """exa_json_path=$.ACCOUNT_DOMAIN,exa_field_name=account_domain""",
    """exa_json_path=$.EVENT_NUMBER,exa_field_name=event_code""",
    """exa_json_path=$.FORMAT_MESSAGE,exa_field_name=additional_info""",
    """exa_json_path=$.ACTIVITY,exa_field_name=operation""",
    """exa_json_path=$.ACTOR_NAME,exa_field_name=service_name""",
    """exa_json_path=$.TARGET1_RES_TYPE,exa_field_name=resource_type""",
    """exa_json_path=$.TARGET1_NAME,exa_field_name=resource_name""",
    """exa_json_path=$.RECORD_NUMBER,exa_field_name=event_id""",
    """exa_json_path=$.REMARKS,exa_field_name=event_name""",
    """exa_json_path=$.ACCOUNT_NAME,exa_regex=(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_json_path=$.CALLER_USER_NAME,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_json_path=$.CALLER_USER_SID,exa_field_name=user_sid""",
    """exa_json_path=$.CALLER_USER_DOMAIN,exa_field_name=domain""",
    """exa_json_path=$.CALLER_LOGON_ID,exa_field_name=login_id""",
    """exa_json_path=$.CALLER_MACHINE_NAME,exa_field_name=src_host""",
    """exa_json_path=$.ACCOUNT_SID,exa_field_name=dest_user_sid""",
    """exa_json_path=$.EVENT_TYPE_TEXT,exa_field_name=result"""
  
}
```