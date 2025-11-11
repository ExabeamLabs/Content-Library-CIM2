#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-endpoint-success-4624-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """CEF:"""
  """"eventID":"4624""""
  """An account was successfully logged on"""
]
Fields = [
  """"systemTime":"({time}\d+-\d+-\d+T\d+:\d+:\d+)"""
  """"computer":"({dest_host}({host}[\w\-.]+))"""
  """"message":"({event_name}[^"]+?)\s*""""
  """"eventID":"({event_code}\d+)"""
  """"eventRecordID":"({event_id}\d+)"""
  """"severityValue":"({result}[^"]+?)\s*""""
  """"subjectUserSid":"({user_sid}[^"\s]+?)\s*""""
  """"subjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*""""
  """"subjectDomainName":"({src_domain}({domain}[^"\s]+?))\s*""""
  """"subjectLogonId":"({login_id}[^"\s]+?)\s*""""
  """"logonType":"({login_type}\d+?)\s*""""
  """"logonProcessName":"({auth_process}[^"]+?)\s*""""
  """"authenticationPackageName":"({auth_package}[^"]+?)\s*""""
  """"workstationName":"({src_host_windows}[^"]+?)\s*""""
  """"processName":"(?:-|({process_path}({process_dir}[^"]*?)(\\+({process_name}[^"\\]+?))?))\s*""""
  """"ipAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"ipPort":"({src_port}\d+)"""
]
ParserVersion = "v1.0.0"


}
```