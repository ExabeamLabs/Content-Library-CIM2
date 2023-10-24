#### Parser Content
```Java
{
Name = "imperva-securesphere-kv-alert-trigger-success-sql"
Vendor = "Imperva"
Product = "Imperva SecureSphere"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """IMPERVA-Imperva,"""
  """,alertSev="""
  """,ruleName ="""
  """,eventType=sql"""
]
Fields = [
  """\Wevent#?=({alert_id}\d+)"""
  """\W(C|c)reateTime=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
  """\WalertSev=(|({alert_severity}.+?))(,\w+=|\s*$)"""
  """\Wgroup=(|({server_group}.+?))(,\w+=|\s*$)"""
  """\WruleName =\"({alert_name}[^\"]+)\""""
  """\WevntDesc=\"({additional_info}[^\"]+)\""""
  """\Wproto=(|({protocol}.+?))(,\w+=|\s*$)"""
  """\WsrcPort=({src_port}\d+)"""
  """\WsrcIP=(?:0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
  """\WsrcHost=\[?({src_host}[\w\-.]+)"""
  """\WdstPort=({dest_port}\d+)"""
  """\WdstIP=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\Wusername=(?:hashed user|nt authority\\anonymous logon|(({domain}[^\\,]+)\\)?({user}[\w\.\-]{1,40}\$?))(,\w+=|\s*$)"""
  """\WdbUsername=(?:nt authority\\anonymous logon|(({domain}[^\\,]+)\\)?({db_user}[^,\\]+?))(,\w+=|\s*$)"""
  """\WdbName =(|({db_name}[^,]+?))(,\w+=|\s*$)"""
  """\Wapplication=\"({process_name}[^\"]+)\""""
  """\WpolicyName =\"({policy_name}[^\"]+)\""""
  """\Waction=\"({action}[^\"]+)\""""
]
DupFields = [
  "alert_name->alert_type"
]
SOAR {
  IncidentType = "generic"
  DupFields = [
    "time->startedDate"
    "vendor->source"
    "rawLog->sourceInfo"
    "alert_name->description"
    "alert_severity->sourceSeverity"
    "alert_id->sourceId"
  ]
  NameTemplate = "Imperva SecureSphere Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "device"
      Name = "src_address"
      Fields = [
        "src_ip->ip_address"
      ]
    

}
```