#### Parser Content
```Java
{
Name = microsoft-evsystem-kv-endpoint-login-success-7001
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  Conditions = [ """eventid="7001"""", """Microsoft-Windows-Winlogon""" ]
  Fields = ${WindowsParsersTemplates.windows-events-2.Fields}[
    """({event_name}User Logon Notification for Customer Experience Improvement Program)""",
  ]

windows-events-2 = {
 Vendor = Microsoft
 Product = Windows
 TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
 Fields = [
   """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)(\.\d+Z)?\s*({host}[^\s]+)\s"""
   """timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
   """"EventID"+:"+({event_code}\d+)""",
   """"subject.logon_id"+:"+({login_id}[^"]+)""",
   """"subject.security_id"+:"+({user_sid}[^"]+)""",
   """"process_information.process_name"+:"+({process_path}({process_dir}[^"]*)\\\\({process_name}[^"]+))""",
   """"process_information.process_id"+:"+({process_id}[^"]+)""",
   """"Computer"+:"+({host}[^"]+)""",
   """"subject.account_name"+:"+(-|({email_address}({user}[\w\.\-]{1,40}\$?)@({domain}[^"]+))|({=user}[^"]+))""",
   """"network_information.source_port"+:"+(-|({src_port}\d+))""",
   """"new_logon.account_domain"+:"+({domain}[^"]+)""",
   """"message"+:"+({additional_info}[^"]+)""",
   """"ProviderName"+:"+({provider_name}[^"]+)""",
   """"logon_information.logon_type"+:"+({login_type}\d+)"""

   """exa_json_path=$.log.timestamp,exa_field_name=time"""
   """exa_json_path=$.log.jsonPayload.EventID,exa_field_name=event_code"""
   """exa_json_path=$.log.jsonPayload.['subject.logon_id'],exa_field_name=login_id"""
   """exa_json_path=$.log.jsonPayload.['subject.security_id'],exa_field_name=user_sid"""
   #"""exa_json_path=$.process_information.process_name,exa_field_name=process_path"""
   #"""exa_json_path=$.process_information.process_id,exa_field_name=process_id"""
   """exa_json_path=$.log.jsonPayload.Computer,exa_field_name=host"""
   """exa_json_path=$.log.jsonPayload.['subject.account_name'],exa_regex=(-|({email_address}({user}[\w\.\-]{1,40}\$?)@({domain}[^"]+))|({=user}[^"]+))"""
   #"""exa_json_path=$.network_information.source_port,exa_field_name=src_port"""
   #"""exa_json_path=$.new_logon.account_domain,exa_field_name=domain"""
   """exa_json_path=$.log.jsonPayload.message,exa_field_name=additional_info"""
   """exa_json_path=$.log.jsonPayload.ProviderName,exa_field_name=provider_name"""
   #"""exa_json_path=$.logon_information.logon_type,exa_field_name=login_type"""
   """exa_json_path=$.log.jsonPayload.privileges,exa_field_name=privileges"""
 
}
```