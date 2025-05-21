#### Parser Content
```Java
{
Name = rsa-ram-kv-app-login-success-singlepoint
  ParserVersion = v1.0.0
  Conditions = [ """ SINGLEPOINT """, """ USER_AUTHZ """ ]
  Fields = ${DLRSAParserTemplate.rsa-system-events.Fields}[
    """userPrincipalName =({email_address}[^@,=]+@[^,=]+?)\s*\,""",
    """displayName =({full_name}[^=]+?)\,\w+=""",
    """ipAddress=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """UserAgent=({user_agent}[^=]+?)\,\w+="""
  ]


}
```