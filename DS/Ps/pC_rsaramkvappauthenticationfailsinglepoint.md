#### Parser Content
```Java
{
Name = rsa-ram-kv-app-authentication-fail-singlepoint
  ParserVersion = v1.0.0
  Conditions = [ """ SINGLEPOINT """, """ RADIUS_USER_LDAP_AUTHENTICATION """, """ STATUS="FAIL"""" ]
  Fields = ${DLRSAParserTemplate.rsa-system-events.Fields}[
    """({operation}RADIUS_USER_LDAP_AUTHENTICATION)""",
    """CLIENT_ID="({client_id}[^"]+)"""",
    """TENANT_ID="({tenant_id}[^"]+)"""",
    """REQUEST_ID="({request_id}[^"]+)"""",
    """NAS-IP-ADDRESS="({nas_ip_address}[A-Fa-f:\d.]+)""",
    """POLICY_ID="({policy_id}[^"]+)""""
  ]


}
```