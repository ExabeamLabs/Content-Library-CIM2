#### Parser Content
```Java
{
Name = "proofpoint-pep-cef-email-send-success-emailquarantine"
Conditions = [
  """CEF:"""
  """|ProofPoint|FilterLog|"""
  """|Email Quarantine|"""
]
ParserVersion = "v1.0.0"

observeit-activity = {
  Vendor = Proofpoint
  Product = ObserveIT
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """"observedAt":\s*"({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """"applicationName":\s*"(?:[A-Fa-f:\d.]+|({app}[^"]+))"""",
    """"command":\s*"({command}[^",]+)"""",
    """"domainName":\s*"({domain}[^",]+)"""",
    """"endpointName":\s*"({host}[^",]+)"""",
    """"loginName":\s*"({user}[\w\.\-]{1,40}\$?)"""",
    """"loginName":\s*"({full_name}\w+\s\w+)"""",
    """"os":\s*"({os}[^",]+)"""",
    """"remoteAddress":\s*"(?:127\.0\.0\.1|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""",
    """"remoteHostName":\s*"(?:\(local\)|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[^",]+))"""",
    """"ruleCategoryName":\s*"({alert_type}[^",]+)"""",
    """"ruleName":\s*"({alert_name}[^",]+)"""",
    """"severity":\s*"({alert_severity}[^",]+)"""",
    """"sessionId":\s*"({session_id}[^",]+)"""",
    """"ruleDesc":\s*"({additional_info}[^"]+?)\s*"""",
    """"detailsUrl":\s*"({additional_info}[^",]+)"""",
    """"sqlUserName":\s*"({db_user}[^",]+)"""",
    """"databaseName":\s*"({db_name}[^",]+)"""",
    """"id":\s*({alert_id}\d+)"""
  
}
```