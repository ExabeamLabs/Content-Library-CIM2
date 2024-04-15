#### Parser Content
```Java
{
Name = "cyberark-pam-kv-alert-trigger-success-nonauthorizedimpersonation"
Conditions = [
"""%CYBERARK:"""
"""Message="Non authorized impersonation """
""";Safe="""
]
DupFields = [
"operation->alert_name"
"operation->alert_type"
]
ParserVersion = "v1.0.0"


}
```