#### Parser Content
```Java
{
Name = "microsoft-mcas-json-alert-trigger-success-mcasalerts"
Vendor = "Microsoft"
Product = "Microsoft CAS"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """dproc=mcas-alerts"""
  """"description":""""
]
Fields = [
  """type":"discovery_ip","label":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """type":"discovery_user","label":"(|({email_address}[^@",]+?@[^@",]+?)|(({domain}[^"\/]+)\/)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
  """\Wsuser=(|({email_address}[^@=]+?@[^@=]+)|({user_uid}(?i)s[^\s]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)"""
  """"timestamp":({time}\d{13})"""
  """"description":"(|\s*({additional_info}[^\}]+?))\s*","""
  """"title":"({alert_name}[^"]+?)(\\u200b)?""""
  """"URL":"({malware_url}[^"]+)"""
  """"severityValue":({alert_severity}\d+)"""
  """"_id":"({alert_id}[^"]+)"""
  """"policyType":"({alert_type}[^"]+)"""
  """"threatScore"+:({original_risk_score}\d+)"""
  """shost=({country_code}[^=]+?)\s\w+="""
  """\srequestClientApplication=({app}[^=]+?)\s+\w+="""
]
DupFields = [ "app->alert_source" ]
ParserVersion = "v1.0.0"


}
```