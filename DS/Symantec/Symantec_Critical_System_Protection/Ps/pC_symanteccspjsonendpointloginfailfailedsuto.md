#### Parser Content
```Java
{
Name = symantec-csp-json-endpoint-login-fail-failedsuto
  Conditions = [ """SVA_IP_ADDRESS: """, """ USER_NAME:""", """failed SU to """ ]
  Fields = ${SymantecParsersTemplates.symantec-critical-sys-protection.Fields}[
    """To Username:\s*({account}[^"\s]+)""",
    """({result}(F|f)ailed)""",
    """Event source:\s*({process_name}[^"]+?)\s*From""",
    """({event_name}failed SU to [^"]+?)\s*Event"""
  ]
  ParserVersion = "v1.0.0"

symantec-critical-sys-protection = {
    Vendor = Symantec
    Product = Symantec Critical System Protection
    TimeFormat = "yyyy-MM-dd HH:mm:ss.S"
    Fields = [
      """\sHOSTNAME\s*:\s*"*({host}[^\s"]+)""",
      """\sEVENT_DT\s*:\s*"*({time}[^"]+)""",
      """\sUSER_NAME\s*:\s*"*({user}[^"\s]+)""",
      """\sRULE_NAME\s*:\s*"*({rule}[^"\s]+)""",
      """\sPOLICY_NAME\s*:\s*"*\s*({policy_name}[^"]+?)\s*"*?\s[^:]+:"""
      """\sPROCESS_PATH\s*:\s*"*({process_name}[^"\s]+)""",
      """SESSION_ID\s*:\s*"*({session_id}\d+)""",
      """Type of login\s*:\s*"*({login_type_text}[^"]+)""",
      """Parent Name\s*:\s*({parent_process}[^\s"]+)""",
      """\sEVENT_ID:\s*"*({event_code}\d+)""",
      """\sHOSTADDR:\s*"*({dest_ip}[^"\s]+)""",
      """\sSVA_IP_ADDRESS:\s*"*({src_ip}[^"\s]+)""",
      """\sDOMAIN_NAME\s*:\s*"*({domain}[^"\s]+)""",
    ]
    DupFields = ["host->src_host"
}
```