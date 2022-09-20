#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-login-success-4624-1
  Conditions = [ """"EVENT_NUMBER":"4624"""", """"REMARKS":"An account was successfully logged on."""" ]
  Fields = ${ADAuditParserTemplates.ad-audit-json-events.Fields}[
    """"CLIENT_HOST_NAME":"(-|({src_ip}(\d{1,3}\.){3}\d{1,3})|({src_host}[^"]+))"""",
    """"CLIENT_IP_ADDRESS":"({src_ip}[^"]+)"""",
    """"SOURCE":"(-|({dest_host}[^"]+))"""".
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
    """"TIME_GENERATED":"({time}\d+)"""".
    """"CALLER_USER_NAME":"(-|({user}[^"]+))"""".
    """"USERNAME":"({user}[^"]+)"""".
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