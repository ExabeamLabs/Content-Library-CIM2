#### Parser Content
```Java
{
Name = "beyondtrust-sra-kv-endpoint-login-success-challenge"
Conditions = [
""";status=challenge;"""
""";target="""
""";when="""
""";who_ip="""
""";who="""
"""event=login"""
]
ParserVersion = "v1.0.0"

pam-authentication.Fields}[
    """({event_name}LDAP authentication failed)""",
    """({failure_reason}The user entered an incorrect password.)""",
  
}
```