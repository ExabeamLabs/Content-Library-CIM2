#### Parser Content
```Java
{
Name = okta-amfa-json-app-activity-success-appgroup
Vendor = Okta
Product = Okta Adaptive MFA
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
ExtractionType = json
Conditions = [
  """samAccountName":"""
  """windowsDomainQualifiedName"""
]
Fields = [
  """exa_json_path=$.lastUpdated,exa_field_name=time""",
  """exa_json_path=$.profile.samAccountName,exa_field_name=user""",
  """exa_json_path=$.profile.description,exa_field_name=operation""",
  """exa_json_path=$._embedded.app.label,exa_field_name=domain""",
  """exa_json_path=$._embedded.app.id,exa_field_name=object""",
  """exa_json_path=$.type,exa_field_name=object_type""",
  """exa_json_path=$.members,exa_regex=\[({members}[^\]]+?)\s*(\]|$)""",
  """exa_json_path=$.assignedApps,exa_field_name=assigned_apps""",
  """exa_json_path=$._embedded.app.name,exa_field_name=app"""
]
ParserVersion = "v1.0.0"


}
```