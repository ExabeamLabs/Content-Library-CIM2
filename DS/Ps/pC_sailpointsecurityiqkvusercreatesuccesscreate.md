#### Parser Content
```Java
{
Name = sailpoint-securityiq-kv-user-create-success-create
Conditions = [
  """| applicationtype : Active Directory |"""
  """actiontype : Create"""
  """| objectclass : user |"""
]
DupFields = [
  "host->dest_host"
  "domain->account_used_domain"
  "user->account",
  "account_name->dest_user"
]
ParserVersion = "v1.0.0"


}
```