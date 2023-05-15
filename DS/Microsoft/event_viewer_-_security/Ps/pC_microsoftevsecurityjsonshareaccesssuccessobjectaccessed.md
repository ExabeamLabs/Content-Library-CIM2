#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-share-access-success-objectaccessed
  ParserVersion = v1.0.0
  Conditions = [ """"EVENT_NUMBER":"5140"""", """"REMARKS":"A network share object was accessed."""" ]
  Fields = ${ADAuditParserTemplates.ad-audit-json-events.Fields}[
    """"CLIENT_HOST_NAME":"(-|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[^"]+))"""",
    """"CLIENT_IP_ADDRESS":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"SOURCE":"(-|({dest_host}[^"]+))"""".
    """"OBJECT_NAME":"[\\?]*(|(({share_path}(({d_parent}[^"]+)\\)?(|({d_name}[^\\"]+?)))\\?))",""",
    """"FILE_NAME":"({file_name}[^"]+?(\.({file_ext}[^\."]+))?)"""",
    """"FILE_LOCATION":"(-|({file_dir}[^"]+))"""",
    """"ACCESSES":"({access}[^"]+)""""
  ]

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