#### Parser Content
```Java
{
Name = "microsoft-windows-kv-endpoint-login-fail-failure"
Vendor = "McAfee"
Product = "McAfee Enterprise Security Manager"
TimeFormat = "epoch"
Conditions = [
  """|McAfee|ESM"""
  """43-211005"""
  """failure"""
]
Fields = [
  """({event_name}Logon Failure)"""
  """\|McAfee\|[^|]+?\|[^|]+?\|43-21100({event_code}\d+)(0|1)\|"""
  """\srt=({time}\d{13})"""
  """deviceTranslatedAddress=({host}[a-fA-F:\d.]+)"""
  """sntdom=({domain}[^\s]+)"""
  """nitroLogon_Type=({login_type}\d+)"""
  """nitroAppID=({auth_package}[^\s]+)"""
  """suser=({src_user}.+?)\s+\w+="""
  """suser=({user}[\w\.\-]{1,40}\$?)\s+\w+="""
  """duser=({user}[\w\.\-]{1,40}\$?)\s+\w+="""
  """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """nitroSource_Logon_ID=\([^,]+,({login_id}[^\)]+)"""
  """nitroDestination_Logon_ID=({login_id}\d+)"""
]
DupFields = [
  "host->dest_host"
  "event_code->result_code"
]
ParserVersion = "v1.0.0"


}
```