#### Parser Content
```Java
{
Name = "vmware-idm-json-app-activity-success-samlartifactcreate"
Conditions = [
""""objectType"""
"""vidm"""
""""organizationId"""
""""SAML_ARTIFACT_CREATE\""""
]
ParserVersion = "v1.0.0"

airwatch-app-activity.Fields}[
    """Timestamp: ({time}\w+\s\d{1,2}\s\d+:\d+:\d+)"""
    """({result}AdminUserLoggedIn)"""
  
}
```