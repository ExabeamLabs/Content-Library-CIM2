#### Parser Content
```Java
{
Name = "vmware-idm-json-app-activity-success-activationtoken"
Conditions = [
""""objectType"""
"""vidm"""
""""organizationId"""
""""ActivationToken\""""
]
ParserVersion = "v1.0.0"

airwatch-app-activity.Fields}[
    """Timestamp: ({time}\w+\s\d{1,2}\s\d+:\d+:\d+)"""
    """({result}AdminUserLoggedIn)"""
  
}
```