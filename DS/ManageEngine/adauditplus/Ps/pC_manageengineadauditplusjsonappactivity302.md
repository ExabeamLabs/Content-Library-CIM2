#### Parser Content
```Java
{
Name = "manageengine-adauditplus-json-app-activity-302"
  Vendor = ManageEngine
  Product = ADAuditPlus
  ExtractionType = json
  TimeFormat = "epoch"
  Conditions = [ """"EVENT_NUMBER":"302"""", """"Category":"AzureADLogonReports"""", """adaudit""" ]
  Fields = [
    """exa_json_path=$.Category,exa_field_name=category""",
    """exa_json_path=$.USER_ON_SID,exa_field_name=user_sid""",
    """exa_json_path=$.FAILURE_REASON,exa_field_name=failure_reason""",
    """exa_json_path=$.MFA_AUTH_DETAILS,exa_field_name=auth_method""",
    """exa_json_path=$.USER_ID,exa_field_name=user_id""",
    """exa_json_path=$.source,exa_field_name=log_source""",
    """exa_json_path=$.LOCATION_STATE,exa_field_name=location_state""",
    """exa_json_path=$.ERROR_CODE,exa_field_name=result_code""",
    """exa_json_path=$.LOGON_TYPE,exa_field_name=login_type_text""",
    """exa_json_path=$.TIME_GENERATED,exa_field_name=time""",
    """exa_json_path=$.LOCATION_CITY,exa_field_name=location_city""",
    """exa_json_path=$.host,exa_field_name=host""",
    """exa_json_path=$.RECORD_ID,exa_field_name=event_id""",
    """exa_json_path=$.USER_PRINCIPAL_NAME,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_json_path=$.USER_DISPLAY_NAME,exa_field_name=full_name""",
    """exa_json_path=$.sourcetype,exa_field_name=protocol""",
    """exa_json_path=$.APP_ID,exa_field_name=app_id""",
    """exa_json_path=$.LOCATION_COUNTRY,exa_field_name=location_country""",
    """exa_json_path=$.REPORT_PROFILE,exa_field_name=action""",
    """exa_json_path=$.APP_DISPLAY_NAME,exa_field_name=client_name""",
    """exa_json_path=$.DEVICE_INFO,exa_regex=({device_name}[^;"]+)""",
    """exa_json_path=$.ACCOUNT_DOMAIN,exa_field_name=account_domain""",
    """exa_json_path=$.LOGIN_STATUS,exa_field_name=result""",
    """exa_json_path=$.EVENT_NUMBER,exa_field_name=event_code""",
    """exa_json_path=$.FORMAT_MESSAGE,exa_field_name=additional_info""",
    """exa_json_path=$.IP_ADDRESS,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.MFA_AUTH_METHOD,exa_field_name=auth_method""",
    """exa_json_path=$.MFA_RESULT,exa_field_name=result_reason"""
    """exa_regex="DEVICE_INFO":"({dest_host}[^";]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```