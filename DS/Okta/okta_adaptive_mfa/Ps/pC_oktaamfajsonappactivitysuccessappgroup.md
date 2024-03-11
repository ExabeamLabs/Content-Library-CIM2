#### Parser Content
```Java
{
Name = okta-amfa-json-app-activity-success-appgroup
Vendor = Okta
Product = Okta Adaptive MFA
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """samAccountName":"""
  """windowsDomainQualifiedName"""
]
Fields = [
  """lastUpdated":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""
  """samAccountName":\s*"({user}[^"]+)"""
  """description":\s*"({operation}[^"]+)"""
  """label":\s*"({domain}[^"]+)"""
  """name".*?,\s*"id":\s*"({object}[^"]+)"""
  """type":\s*"({object_type}[^"]+)"""
  """members":\s*\[({members}[^\]]+?)\s*(\]|$)"""
  """assignedApps":\s*\[(:-?|({assigned_apps}[^\]]+))"""
  """"app":\s\{.*?"name":\s*"({app}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```