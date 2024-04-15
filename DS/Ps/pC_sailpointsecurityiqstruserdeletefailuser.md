#### Parser Content
```Java
{
Name = "sailpoint-securityiq-str-user-delete-fail-user"
Conditions = [
"""| applicationtype : Active Directory |"""
"""actiontype : Delete"""
"""| objectclass : user |"""
]
DupFields = [
"host->src_host"
]
ParserVersion = "v1.0.0"


}
```