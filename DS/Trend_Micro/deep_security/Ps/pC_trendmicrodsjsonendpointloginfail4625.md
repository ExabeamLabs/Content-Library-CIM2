#### Parser Content
```Java
{
Name = trendmicro-ds-json-endpoint-login-fail-4625
  ParserVersion = v1.0.0
  Conditions = [ """"OSSEC_Log""", """"Origin\":0""", """"EventType\":\"LogInspectionEvent""", """An account failed to log on""", """4625""" ]
  Fields = ${TrendMicroParserTemplates.trendmicro-ds-ossecevents.Fields}[
    """({event_name}An account failed to log on)""",
    """Subject(:|=).+?Account Name(:|=)\s*(-|({src_user}[^\s@]+?))[\s;]*Account Domain(:|=)""" 
    """Subject(:|=).+?Account Domain(:|=)\s*(-|({src_domain}[^:;]+?))[\s;]*Logon ID(:|=)"""  
    """Logon Type(:|=)\s*({login_type}\d+)""" 
    """Account For[\s;]*Which Logon Failed(:|=)[\s;]*Security ID(:|=)\s*([\/\\]{0,9}NULL SID|({user_sid}[^=:]+?))[\s;]*Account Name"""  
    """Logon Failed(:|=).+?Account Name(:|=)\s*(-|SYSTEM|d2\/|({email_address}[^\s@;]+?@[^\s@;]+?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))[\s;]*Account Domain(:|=)"""  
    """Logon Failed(:|=).+?Account Domain(:|=)\s*(|-|\?|({domain}[^\s]+?))[\s;]*Failure Information""" 
    """Sub Status(:|=)\s*({failure_code}({result_code}[^\s;]+?))[\s;]*Process Information(:|=)""" 
    """Workstation Name(:|=)\s*(?:-|(::ffff:)?({src_host}({src_host_windows}[\w\-\.]+)))[\s;]*Source Network Address(:|=)"""  
    """Source Network Address(:|=)\s*(?:-|(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)[\s;]*Source Port(:|=)"""  
    """Logon Process(:|=)\s*({auth_process}[^\s;]+)[\s;]*Authentication Package(:|=)""" 
    """Authentication Package(:|=)\s*({auth_package}[^\s;]+?)[\s;]*Transited Services(:|=)"""
    """Failure Reason:\s*({failure_reason}[^\.]+)\s*"""
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