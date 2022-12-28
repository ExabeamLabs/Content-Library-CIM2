#### Parser Content
```Java
{
Name = symantec-csp-kv-configuration-modify-success-primarygroupchanged
ParserVersion = "v1.0.0"
Conditions = [ """SVA_IP_ADDRESS: """, """ USER_NAME:""", """User_Primary_Group_Changed""" ]
Fields = ${SymantecParsersTemplates.symantec-critical-sys-protection.Fields} [
  """({event_name}User_Primary_Group_Changed)""",
  """User Primary Group ID for "+({user}[^\s"]+)"+ CHANGED from .+ in ({object}[^\s"]+)"*""",
  """({old_attribute}Old Entry: [^\s]+)""",
  """({new_attribute}New Entry: [^"]+)"""
]
DupFields = ["object->group_name"]

symantec-critical-sys-protection = {
    Vendor = Symantec
    Product = Symantec Critical System Protection
    TimeFormat = "yyyy-MM-dd HH:mm:ss.S"
    Fields = [
      """\sHOSTNAME\s*:\s*"*({host}[^\s"]+)""",
      """\sEVENT_DT\s*:\s*"*({time}[^"]+)""",
      """\sUSER_NAME\s*:\s*"*({user}[^"\s]+)""",
      """\sRULE_NAME\s*:\s*"*({rule}[^"\s]+)""",
      """\sPOLICY_NAME\s*:\s*"*\s*({policy_name}[^"]+)\s*"*?\s[^:]+:"""
      """\sPROCESS_PATH\s*:\s*"*({process_name}[^"\s]+)""",
      """SESSION_ID\s*:\s*"*({session_id}\d+)""",
      """Type of login\s*:\s*"*({login_type_text}[^"]+)""",
      """Parent Name\s*:\s*({parent_process}[^\s"]+)""",
      """\sEVENT_ID:\s*"*({event_code}\d+)""",
      """\sHOSTADDR:\s*"*({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """\sSVA_IP_ADDRESS:\s*"*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """\sDOMAIN_NAME\s*:\s*"*({domain}[^"\s]+)""",
    ]
    DupFields = ["host->dest_host"
}
```