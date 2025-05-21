#### Parser Content
```Java
{
Name = "microsoft-o365-mix-app-activity-success-securitycompliancecenter"
ExtractionType = json
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSS", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd HH:mm:ss.SSS", "yyyy-MM-dd'T'HH:mm:ssZ"]
Conditions = [
  """SecurityComplianceCenter"""
  """Workload"""
  """Operation"""
]
Fields = [
  """"CreationTime":"({time}\d\d\d\d-\d\d-\d\d\s*\d\d:\d\d:\d\d\.\d\d\d)""""
  """CreationTime"*:\s*"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """CreationTime"*:\s*"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,7})?Z)"""
  """Operation"*:\s*"+({operation}[^"]+)"*"""
  """destinationServiceName =({app}[^=]+?)\s+\w+="""
  """Workload"*:\s*"*({app}[^"]+)"""
  """"ObjectId":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)",""""
  """"f3u\\?":\\?"({email_address}[^@"]+@[^",\.]+\.[^",]+?)\\?""""
  """trc\\*"+:\\*"+({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
  """"app-user-displayname":"({full_name}[^"]+)""",
  """"user-email":"({email_address}[^",@]+@[^",\.]+\.[^",]+)"""
  """"ResultStatus":"({result}[^"]+)"""
  """"src-account-name":"({account}[^"]+)"""
  """"UserType":\s*"*({user_type}[^\}"]+)\s*"*(,|\})"""
  """"UserId":\s*"({user_upn}[^,"]+)""""
  """"sip\\*":\\*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.CreationTime,exa_field_name=time"""
  """exa_regex=CreationTime":"({time}\d\d\d\d-\d\d-\d\d\s*\d\d:\d\d:\d\d\.\d\d\d)""""
  """exa_regex="CreationTime"*:\s*"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """exa_regex=CreationTime"*:\s*"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,7})?Z)"""
  """exa_regex=Operation"*:\s*"+({operation}[^"]+)"*"""
  """exa_json_path=$.Operation,exa_field_name=operation"""
  """exa_regex=destinationServiceName =({app}[^=]+?)\s+\w+="""
  """exa_json_path=$.Workload,exa_field_name=app"""
  """exa_regex"Workload"*:\s*"*({app}[^"]+)"""
  """exa_json_path=$..['Workload'],exa_field_name=app"""
  """exa_regex="f3u\\?":\\?"({email_address}[^@"]+@[^",\.]+\.[^",]+?)\\?""""
  """exa_regex=trc\\*"+:\\*"+({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
  """exa_json_path=$.app-user-displayname,exa_field_name=full_name"""
  """exa_json_path=$.ResultStatus,exa_field_name=result"""
  """exa_regex="src-account-name":"({account}[^"]+)"""
  """exa_regex="UserId":\s*"(NOT-FOUND|SecurityComplianceAlerts|SecurityComplianceInsights|(\w+\-){4}\w+|({user_upn}[^",]+))""""
  """exa_regex="sip\\*":\\*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_regex="UserType":\s*"*({user_type}[^\}"]+)\s*"*(,|\})"""
]
ParserVersion = "v1.0.0"


}
```