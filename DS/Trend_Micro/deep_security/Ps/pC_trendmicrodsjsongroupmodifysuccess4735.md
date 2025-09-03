#### Parser Content
```Java
{
Name = trendmicro-ds-json-group-modify-success-4735
  ParserVersion = v1.0.0
  Conditions = [ """"OSSEC_Log""", """"Origin\":0""", """"EventType\":\"LogInspectionEvent""", """A security-enabled local group was changed""", """4735""" ]
  Fields = ${TrendMicroParserTemplates.trendmicro-ds-ossecevents.Fields}[
    """({event_name}A security-enabled local group was changed)""",
    """Group:\s+Security ID:\s+({group_id}[^\s]+)""",
    """Group:.+?(Group|Account) Name:\s+({group_name}.+?)?\s+(Group|Account) Domain:""",
    """Group:.+?(Group|Account) Domain:\s+({group_domain}[^\s]+)"""
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