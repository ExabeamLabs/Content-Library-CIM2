#### Parser Content
```Java
{
Name = ibm-sbi-str-app-authentication-success-authenticationpolicy
  Vendor = IBM
  Product = Sterling B2B Integrator
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """ LDAPAuthentication """, """LDAP Authentication Policy""",  """sterling"""]
  Fields = [
    """\s+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\+\d\d:\d\d)\s+\w+\s+sterling(?:\s-){3}""",
    """LDAPAuthentication.+?used by\s+({user_id}[^\.]+)""",
    """LDAPAuthentication\s+({description}[^\,]+)""",
    """({event_name}LDAP Authentication Policy)""",
  ]
  ParserVersion = "v1.0.0"


}
```