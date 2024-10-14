#### Parser Content
```Java
{
Name = trendmicro-ds-json-service-create-success-7045
  ParserVersion = v1.0.0
  Conditions = [ """"OSSEC_Log""", """"Origin\":0""", """"EventType\":\"LogInspectionEvent""", """A service was installed in the system""", """7045""" ]
  Fields = ${TrendMicroParserTemplates.trendmicro-ds-ossecevents.Fields}[
    """({event_name}A service was installed in the system)"""
    """\sService Name:\s*(|({service_name}[^:]+?)(_[0-9a-f]+)?)\s"""
    """\sService Type:\s*(|({service_type}.+?))(\\[nrt]\s+|\s)"""
    """\sService File Name:\s*\"*(|({process_path}({process_dir}.*?[\\\/]+)?({process_name}[^\\\/\"]+?)))\"*\s"""
    """\sService Start Type:\s*(|({service_start_type}.+?))(\\[nrt]\s+|\s)"""
    """\sService Account:\s*(({account_domain}[^\\"\s]+)\\)?({account_name}[^"\s]+)"""
  ]

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