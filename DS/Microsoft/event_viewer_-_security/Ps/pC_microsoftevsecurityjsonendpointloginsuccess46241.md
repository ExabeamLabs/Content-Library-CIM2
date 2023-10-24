#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-login-success-4624-1
  Conditions = [ """"EVENT_NUMBER":"4624"""", """"REMARKS":"An account was successfully logged on."""" ]
  Fields = ${ADAuditParserTemplates.ad-audit-json-events.Fields}[
    """"CLIENT_HOST_NAME":"(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[^"]+))"""",
    """"CLIENT_IP_ADDRESS":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"SOURCE":"(-|({dest_host}[\w\-.]+))"""".
    """"USER_SAM_ACCOUNT_NAME":"(null|({account}[^"]+))"""".
    """"KEY_LENGTH":"({key_length}\d+)"""",
    """"LOGON_PROCESS":"({auth_process}[^"]+)"""",
    """"AUTHENTICATION_PACKAGE":"({auth_package}[^"]+)"""".
    """"CALLER_PROCESS_NAME":"(-|({process_path}[^"]+))"""",
    """"RECORD_NUMBER":"({event_id}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"

ad-audit-json-events = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "epoch_sec"
  Fields = [
    """"TIME_GENERATED":"({time}\d{10})"""".
    """"CALLER_USER_NAME":"(-|({user}[\w\.\-]{1,40}\$?))"""".
    """"USERNAME":"({user}[\w\.\-]{1,40}\$?)"""".
    """"LOGON_TYPE":"({login_type}\d+)"""".
    """"REMARKS":"({event_name}[^"]+)"""".
    """"EVENT_NUMBER":"({event_code}\d+)"""".
    """"DOMAIN":"({domain}[^"]+)"""",
    """"(SOURCE|CLIENT)_PORT":"({src_port}\d+)"""".
    """"WORKSTATION_NAME":"(-|({src_host_windows}[^"]+))"""",
    """"LOGON_ID":"({login_id}[^"]+)"""",
    """"USER_SID":"({user_sid}[^"]+)"""",
    """"ERROR_CODE":"(null|({result_code}[^"]+))"""",
    """"EVENT_TYPE_TEXT":"({result}[^"]+)""""
  
}
```