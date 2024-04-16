#### Parser Content
```Java
{
Name = "logmein-ra-json-endpoint-login-success-raloginsuccess"
Vendor = "LogMeIn"
Product = "RemotelyAnywhere"
TimeFormat = "yyyy-MM-dd HH:mm:ss.S"
Conditions = [
  """"Windows_Remotely_Anywhere_Policy"""
  """ POLICY_NAME: """
  """RA_Login_Success"""
]
Fields = [
  """EVENT_DT:\s"+({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\.\d)""""
  """\sHOSTADDR:\s"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
  """\sHOSTNAME:\s+"+({host}[^"]+)"+\s"""
  """\sSession\s-\s({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\s-\sLogging in as '(({domain}\w+)\\)?({user}[\w\.\-]{1,40}\$?)'."""
  """\sDESCRIPTION:\s"+({description}[^"]+)""""
  """\sRULE_NAME: "*({rule}[^"]+)""""
  """\sDOMAIN_NAME:\s+"+(unknown|null|({domain}[^"]+))"+\s"""
  """\sEVENT_TYPE_D:\s+"+({event_name}[^"]+)"+\s"""
  """\sEVENT_SEVERITY_D:\s+"+({alert_severity}[^"]+)"+\s"""
  """\sEVENT_PRIORITY:\s+"+({priority}[^"]+)"+\s"""
  """\sPOLICY_NAME:\s+"+({policy_name}[^"]+)"+\s"""
  """\sPROCESS_NAME:\s+"+(unknown|null|({process_path}[^"]+))"+\s"""
  """\sUSER_NAME:\s+"+(unknown|null|({user}[\w\.\-]{1,40}\$?))"+\s"""
]
DupFields = [
  "event_name->event_category"
]
ParserVersion = "v1.0.0"


}
```