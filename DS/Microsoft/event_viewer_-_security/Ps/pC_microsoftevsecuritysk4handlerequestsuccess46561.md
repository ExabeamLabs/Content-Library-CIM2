#### Parser Content
```Java
{
Name = microsoft-evsecurity-sk4-handle-request-success-4656-1
  Vendor = Microsoft
  Product = event viewer - security
  TimeFormat = "epoch_sec"
  Conditions = [ """"EVENT_NUMBER":"4656"""", """"REMARKS":"A handle to an object was requested."""" ]
  Fields = [
    """"TIME_GENERATED":"({time}\d{10})"""".
    """"CALLER_USER_NAME":"(-|({user}[^"]+))"""".
    """"USERNAME":"({user}[^"]+)"""".
    """"LOGON_TYPE":"({login_type}\d+)"""".
    """"REMARKS":"({event_name}[^"]+)"""".
    """"EVENT_NUMBER":"({event_code}\d+)"""".
    """"DOMAIN":"({domain}[^"]+)"""",
    """"CLIENT_HOST_NAME":"(-|({dest_ip}(\d{1,3}\.){3}\d{1,3})|({src_host}[^"]+))"""",
    """"CLIENT_IP_ADDRESS":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"SOURCE":"({src_host}[^"]+)"""".
    """"ACCESSES":"({access}[^"]+)"""",
    """"ACCESS_MASK":"({access_mask}[^"]+)"""",
    """"FILE_NAME":"({file_name}[^"]+)"""",
    """"FILE_LOCATION":"({file_dir}[^"]+)"""",
    """"FILE_TYPE":"({file_type}[^"]+)"""",
    """"HANDLE_ID":"({object_id}[^"]+)"""",
    """"OBJECT_NAME":"({object}[^"]+)"""",
    """"PROCESS_NAME":"({process_path}[^"]+)"""",
    """"PROCESS_ID":"({process_id}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```