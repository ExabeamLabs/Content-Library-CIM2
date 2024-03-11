#### Parser Content
```Java
{
Name = rsa-ram-kv-app-authentication-success-radius
  Conditions = [ """ SINGLEPOINT """, """ RADIUS_USER_LDAP_AUTHENTICATION """, """ STATUS="SUCCESS"""" ]
  Fields = ${DLRSAParserTemplate.rsa-system-events.Fields}[
    """({operation}RADIUS_USER_LDAP_AUTHENTICATION)""",
    """CLIENT_ID="({client_id}[^"]+)"""",
    """TENANT_ID="({tenant_id}[^"]+)"""",
    """REQUEST_ID="({request_id}[^"]+)"""",
    """NAS-IP-ADDRESS="({nas_ip_address}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """POLICY_ID="({policy_id}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```