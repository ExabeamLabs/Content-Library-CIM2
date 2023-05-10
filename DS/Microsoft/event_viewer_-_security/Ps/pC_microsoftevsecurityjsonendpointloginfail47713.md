#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-login-fail-4771-3
  Conditions = [ """"EVENT_NUMBER":"4771"""", """"REMARKS":"Kerberos pre-authentication failed."""" ]
  Fields = ${ADAuditParserTemplates.ad-audit-json-events.Fields}[
    """"CLIENT_HOST_NAME":"(-|({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[^"]+))"""",
    """"CLIENT_IP_ADDRESS":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"SOURCE":"(-|({src_host}[^"]+))"""".
    """"RECORD_NUMBER":"({event_id}[^"]+)""""
  ]
  DupFields = [
    "result_code->failure_code"
  ]
  ParserVersion = "v1.0.0"

ad-audit-json-events = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "epoch_sec"
  Fields = [
    """"TIME_GENERATED":"({time}\d{10})"""".
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