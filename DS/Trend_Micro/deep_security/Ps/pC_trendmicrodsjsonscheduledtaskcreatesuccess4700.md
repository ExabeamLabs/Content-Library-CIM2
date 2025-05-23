#### Parser Content
```Java
{
Name = trendmicro-ds-json-scheduled-task-create-success-4700
  ParserVersion = v1.0.0
  Conditions = [ """"OSSEC_Log""", """"Origin\":0""", """"EventType\":\"LogInspectionEvent""", """A scheduled task was enabled""", """4700""" ]
  Fields = ${TrendMicroParserTemplates.trendmicro-ds-ossecevents.Fields}[
    """({event_name}A scheduled task was enabled)""",
    """"TaskName":"({task_name}[^"]+)""""
  ]

trendmicro-ds-ossecevents = {
   Product = Deep Security
   Vendor = Trend Micro
   TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
   Fields = [
      """"LogDate\\*":\\*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
      """"EventType\\*":\\*"({event_category}LogInspectionEvent)""",
      """"Hostname\\*":\\*"(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}[\w\-\.]+))""",
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