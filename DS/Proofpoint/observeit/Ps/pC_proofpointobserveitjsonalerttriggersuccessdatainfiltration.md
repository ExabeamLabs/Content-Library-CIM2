#### Parser Content
```Java
{
Name = proofpoint-observeit-json-alert-trigger-success-datainfiltration
  Conditions = [ """"observedAt": """", """"sessionUrl": """", """"loginName": """", """"ruleCategoryName": "DATA INFILTRATION""" ]
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
    """"loginName":\s*"({user}[^",\s]+)"""",
    """"loginName":\s*"({full_name}\w+\s\w+)"""",
    """"os":\s*"({os}[^",]+)"""",
    """"remoteAddress":\s*"(?:127\.0\.0\.1|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""",
    """"remoteHostName":\s*"(?:\(local\)|({src_ip}[A-Fa-f:\d.]+)|({src_host}[^",]+))"""",
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