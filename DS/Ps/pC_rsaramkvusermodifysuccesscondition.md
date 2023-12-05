#### Parser Content
```Java
{
Name = rsa-ram-kv-user-modify-success-condition
  Conditions = [ """ SINGLEPOINT """, """ USER_AUTHN_CONDITION """ ]
  Fields = ${DLRSAParserTemplate.rsa-system-events.Fields}[
    """({operation}USER_AUTHN_CONDITION)""",
    """ipAddress=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """UserAgent=({user_agent}[^=]+?)\,\w+=""",
    """RESOURCE="({app}[^"]+)"""",
    """USER_AUTHN_CONDITION\s+({additional_info}\[[^\}]+?)\]\s*$"""
  ]
  ParserVersion = "v1.0.0"


}
```