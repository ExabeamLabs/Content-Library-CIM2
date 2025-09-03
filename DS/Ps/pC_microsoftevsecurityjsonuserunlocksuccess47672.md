#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-unlock-success-4767-2"
ExtractionType = json
Conditions = [
"""A user account was unlocked"""
"""Account Name:"""
"""computer_name"""
"""event_id":4767"""
]
DupFields = ["user->src_user", "domain->src_domain"]
ParserVersion = "v1.0.0"


}
```