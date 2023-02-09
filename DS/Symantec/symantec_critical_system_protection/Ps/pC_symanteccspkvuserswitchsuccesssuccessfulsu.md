#### Parser Content
```Java
{
Name = symantec-csp-kv-user-switch-success-successfulsu
  Vendor = Symantec
  Product = Symantec Critical System Protection
  TimeFormat = "yyyy-MM-dd HH:mm:ss.S"
  Conditions = [ """SVA_IP_ADDRESS: """, """ USER_NAME:""", """successful SU to """ ]
  Fields = [
    """\sHOSTNAME\s*:\s*"+({host}[^\s"]+)""",
    """\sEVENT_DT\s*:\s*"+({time}[^"]+)""",
    """\sUSER_NAME\s*:\s*"+({user}[^"\s]+)""",
    """\sRULE_NAME\s*:\s*"+({rule}[^"\s]+)""",
    """\sPOLICY_NAME\s*:\s*"+\s*({policy_name}[^"]+?)\s*"+?\s[^:]+:"""
    """\sPROCESS_PATH\s*:\s*"+({process_name}[^"\s]+)""",
    """SESSION_ID\s*:\s*"+({session_id}\d+)""",
    """Type of login\s*:\s*"*({login_type_text}[^"]+)""",
    """Parent Name\s*:\s*({parent_process}[^\s"]+)""",
    """\sEVENT_ID:\s*"+({event_code}\d+)""",
    """\sHOSTADDR:\s*"+({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sSVA_IP_ADDRESS:\s*"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """To Username:\s*({account}[^"\s]+)""",
    """({result}(S|s)uccessful)""",
    """({event_name}successful SU to [^"]+?)\s*Event"""
  ]
  DupFields = ["host->dest_host"]
  ParserVersion = "v1.0.0"


}
```