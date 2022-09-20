#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-file-delete-success-4663-1
  Conditions = [ """"EVENT_NUMBER":"4663"""", """"REMARKS":"An object was deleted."""" ]
  Fields = ${ADAuditParserTemplates.ad-audit-json-events.Fields}[
    """"CLIENT_HOST_NAME":"(-|({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[^"]+))"""",
    """"CLIENT_IP_ADDRESS":"({dest_ip}[a-fA-F\d:.]+)"""",
    """"SOURCE":"(-|({src_host}[^"]+))"""".
    """"OBJECT_NAME":"({file_path}({file_dir}[^"]+)\\+({file_name}[^"]+))""",
    """"FILE_NAME":"({file_name}[^"]+?(\.({file_ext}[^\."]+))?)"""",
    """"ACCESSES":"({access}[^"]+)"""",
    """"ACCESS_MASK":"({access_mask}[^"]+)"""",
    """"PROCESS_NAME":"({process_path}[^"]+)"""",
    """"PROCESS_ID":"({process_id}[^"]+)""""
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