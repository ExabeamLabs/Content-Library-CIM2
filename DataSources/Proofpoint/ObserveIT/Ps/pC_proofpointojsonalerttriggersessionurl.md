#### Parser Content
```Java
{
Name = proofpoint-o-json-alert-trigger-sessionurl
  ParserVersion = "v1.0.0"
  Conditions = [ """"observedAt": """", """"sessionUrl": """", """"loginName": """", """"ruleCategoryName": """" ]

observeit-events = {
    Vendor = Proofpoint
    Product = ObserveIT
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"observedAt":\s*"({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
      """"applicationName":\s*"(?:[A-Fa-f:\d.]+|({app}[^"]+))"""",
      """"command":\s*"({process_command_line}[^",]+)"""",
      """"domainName":\s*"({domain}[^",]+)"""",
      """"endpointName":\s*"({host}[^",]+)"""",
      """"loginName":\s*"({user}[^",\s]+)"""",
      """"loginName":\s*"({full_name}\w+\s\w+)"""",
      """"os":\s*"({os}[^",]+)"""",
      """"remoteAddress":\s*"(?:127\.0\.0\.1|({src_ip}[A-Fa-f:\d.]+))"""",
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