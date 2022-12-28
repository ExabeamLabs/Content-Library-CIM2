#### Parser Content
```Java
{
Name = beyondtrust-b-kv-endpoint-login-success-loggedin
  Vendor = BeyondTrust
  Product = BeyondTrust
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """|Bomgar|Privileged Access|""", """sessionId=""", """dstUser=""" ]
  Fields = [
    """({app}Privileged Access)""",
    """\|Privileged Access\|([^\|]+\|){2}({operation}[^\|]+)\|""",
    """srcAddr=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """srcPort=({src_port}\d+)""",
    """srcHost=({src_host}[^\|]+)""",
    """\|dstUser=(({full_name}({first_name}[^\s\|]+)\s({last_name}[^\|]+))|({user}[^\|]+))""",
    """msg=({additional_info}[^\|]+?)\s*\|""",
    """credentialName =({additional_info}[^\|]+)"""
  ]
  DupFields = [ "operation->event_name" ]
  ParserVersion = "v1.0.0"


}
```