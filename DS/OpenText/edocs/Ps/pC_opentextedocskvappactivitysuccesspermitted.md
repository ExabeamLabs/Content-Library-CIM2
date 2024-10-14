#### Parser Content
```Java
{
Name = "opentext-edocs-kv-app-activity-success-permitted"
Vendor = "OpenText"
Product = "eDOCS"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """Access Permitted"""
  """eDocs"""
  """Activity:"""
]
Fields = [
  """ACTIVITY_DATE:\s*"+({time}\d{4}-\d{2}-\d{2}\s\d{2}:\d{2}:\d{2})"""
  """"+eDocs\s*-\s*({host}[^"]+)"+"""
  """DOCNUMBER:\s*"+({resource}\d+)"+"""
  """Activity:\s*"+({operation}[^"]+)"+"""
  """APPLICATION:\s*"+({app}[^"]+)"+"""
  """DOCNAME:\s*"+({object}[^"]+)"+"""
  """AUTHOR_ID:\s*"+({user_id}[^"]+)"+"""
  """AUTHOR_NAME:\s*"+({full_name}[^"]+)"+"""
  """CLIENT_ID:\s*"+({client_id}[^"]+)"+"""
  """CLIENT_NAME:\s*"+({client_name}[^"]+)"+"""
  """TYPIST_ID:\s*"+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"+"""
]
ParserVersion = "v1.0.0"


}
```