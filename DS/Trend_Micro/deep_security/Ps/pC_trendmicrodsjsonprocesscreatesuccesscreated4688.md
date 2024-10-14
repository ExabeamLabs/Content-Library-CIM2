#### Parser Content
```Java
{
Name = trendmicro-ds-json-process-create-success-created-4688
  ParserVersion = v1.0.0
  Conditions = [ """"OSSEC_Log""", """"Origin\":0""", """"EventType\":\"LogInspectionEvent""", """A new process has been created""", """4688""" ]
  Fields = ${TrendMicroParserTemplates.trendmicro-ds-ossecevents.Fields}[
    """({event_name}A new process has been created)""",
    """New Process Name:(\\*[nrt]|\s)*({dest_process_path}({dest_process_dir}[^"]+?)?[\\]*?({dest_process_name}[^"\\]+?))(\\*[nrt]|\s)*Token Elevation Type:""",
    """New Process ID:((\\)*(\\t|\\r|\\n))*\s*({process_guid}[^\\\s;]+)(\s|;|\\)""",
    """Creator Process ID:\s*({parent_process_guid}[^\\\s;]+)(\s|;|\\)""",
    """Creator Process Name:(\\*[nrt]|\s)*(|({parent_process_path}({parent_process_dir}[^"]+?)?[\\]*?({parent_process_name}[^"\\]+?)))(\\*[nrt]|\s)*Process"""
  ]
  DupFields = [ "process_guid->process_id" ,"parent_process_guid->parent_process_id"]

trendmicro-ds-ossecevents = {
   Product = Deep Security
   Vendor = Trend Micro
   TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
   Fields = [
      """"LogDate\\*":\\*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
      """"EventType\\*":\\*"({event_category}LogInspectionEvent)""",
      """"Hostname\\*":\\*"(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}[\w\-\.]+))""",
      """"HostOS\\*":\\*"({os}[^\\"]+)""",
      """"OSSEC_Hostname\\*":\\*"({host}[\w.-]+)""",
      """"OSSEC_SystemName\\*":\\*"({host}[\w.-]+)""",
      """"TenantId\\*":({tenant_id}\d+)""",
      """"OSSEC_ID\\*":\\*"({event_code}\d+)""",
      """Subject:.+?Security ID:\s*({user_sid}[^\s]+)\s+Account Name:""",
      """Subject:.+?Account Name:\s*(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
      """Subject:.+?Account Domain:\s*(-|({domain}[^\s]+))""",
      """Subject:.+?Logon ID:\s*({login_id}[^\s]+)"""
    
}
```