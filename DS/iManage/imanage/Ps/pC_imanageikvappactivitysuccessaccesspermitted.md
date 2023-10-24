#### Parser Content
```Java
{
Name = imanage-i-kv-app-activity-success-accesspermitted
Vendor = iManage
Product = iManage
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """Access Permitted"""
  """iManage"""
  """ACTIVITY:"""
]
Fields = [
  """ACTIVITY_DATE:\s*"+({time}\d{4}-\d{2}-\d{2}\s\d{2}:\d{2}:\d{2})"""
  """DOCNUMBER:\s*"+({resource}[^"]+)"+"""
  """ACTIVITY:\s"+({operation}[^"]+)"+"""
  """APPNAME:\s*"+({app}[^"]+)"+"""
  """DOCNAME:\s*"+({object}[^"]+)"+"""
  """AUTHOR_NAME:\s*"+({full_name}.+?)\s*"+"""
  """OPERATOR_ID:\s*"+({user}[\w\.\-]{1,40}\$?)"+"""
  """OPERATOR_NAME:\s*"+({operator_name}.+?)\s*"+"""
  """CLIENT_ID:\s*"+({client_id}[^"]+)"+"""
  """CLIENT_NAME:\s*"+({client_name}[^"]+)"+"""
  """SECURED:\s*"+({secured}[^"]+)"+"""
]
ParserVersion = "v1.0.0"


}
```