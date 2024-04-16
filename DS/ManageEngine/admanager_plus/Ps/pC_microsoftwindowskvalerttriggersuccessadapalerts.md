#### Parser Content
```Java
{
Name = "microsoft-windows-kv-alert-trigger-success-adapalerts"
Vendor = "ManageEngine"
Product = "ADManager Plus"
TimeFormat = "epoch_sec"
Conditions = [
  """ADAuditPlus"""
  """Category = ADAPAlerts"""
  """ALERT_PROFILE ="""
]
Fields = [
  """({host}[\w\-.]+) ADAuditPlus"""
  """\WUNIQUE_ID\s*=\s*({alert_id}\d+)"""
  """\WTIME_GENERATED\s*=\s*({time}\d{10})"""
  """\WSOURCE\s*=\s*(?:User Behaviour Analytics|({src_host}[\w\-.]+))"""
  """\WALERT_PROFILE\s*=\s*({alert_type}[^=]+?)\s*(\]|([\w_]+)\s*=)"""
  """\WSEVERITY\s*=\s*({alert_severity}\d+)"""
  """\WFORMAT_MESSAGE\s*=\s*.+?\sby\s+'(({domain}[^'\\]+)\\)?({user}[\w\.\-]{1,40}\$?)'""",
  """\WFORMAT_MESSAGE = User '?({dest_user}[^'\s]+)'?[^=]+?was (created|deleted) by""",
  """\WFORMAT_MESSAGE\s*=\s*.+?\soccured for\s+({user}[\w\.\-]{1,40}\$?)\s"""
  """\WFORMAT_MESSAGE\s*=.+?host:(?:({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[^\s]+))\s+was accessed by user:({user}[\w\.\-]{1,40}\$?)\s"""
  """\WFORMAT_MESSAGE\s*=.+?\sfor User\s*'(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))'\s*in\s*'(?:({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[^\s']+))'"""
  """\WFORMAT_MESSAGE\s*=.+?\swas done by\s+({user}[\w\.\-]{1,40}\$?)\s"""
  """\WFORMAT_MESSAGE\s*=.+?was modified by\s+'(({domain}[^'\\]+)\\)?({user}[\w\.\-]{1,40}\$?)'"""
  """\WFORMAT_MESSAGE\s*=.+?\son\s+'?(?:({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[^\s'\(\)]+))'?\s+"""
  """\WFORMAT_MESSAGE\s*=.+?\s+occured on\s+(?:({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[^\s]+))\s+"""
  """\WDOMAIN\s*=\s*({domain}[^\s\]]+)"""
  """\WFORMAT_MESSAGE\s*=\s*({additional_info}.+?)\s*(\]|([\w_]+)\s+=)"""
]
DupFields = [
  "alert_type->alert_name"
]
ParserVersion = "v1.0.0"


}
```