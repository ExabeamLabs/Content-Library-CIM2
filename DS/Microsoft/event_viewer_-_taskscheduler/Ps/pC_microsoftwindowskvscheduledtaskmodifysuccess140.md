#### Parser Content
```Java
{
Name = microsoft-windows-kv-scheduled-task-modify-success-140
  Product = Event Viewer - TaskScheduler
  ParserVersion = "v1.0.0"
  Conditions = [ """eventid="140"""", """Microsoft-Windows-TaskScheduler""" ]
  Fields = ${WindowsParsersTemplates.windows-events-2.Fields}[
    """({event_name}updated Task Scheduler task)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)(\.\d+Z)?\s*({host}[^\s]+)\s""",
    """"Computer"+:"+({host}[^"]+)""",
    """exa_json_path=$.log.jsonPayload.Computer,exa_field_name=host"""
  ]

windows-events-2 = {
 Vendor = Microsoft
 Product = Windows
 TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
 Fields = [ 
   """timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
   """"EventID"+:"+({event_code}\d+)""",
   """"subject.logon_id"+:"+({login_id}[^"]+)""",
   """"subject.security_id"+:"+({user_sid}[^"]+)""",
   """"process_information.process_name"+:"+({process_path}({process_dir}[^"]*)\\\\({process_name}[^"]+))""",
   """"process_information.process_id"+:"+({process_id}[^"]+)""",
   """"subject.account_name"+:"+(-|({user_upn}({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^"]+))|({=user}[^"]+))""",
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
   """exa_json_path=$.log.jsonPayload.['subject.account_name'],exa_regex=(-|({user_upn}({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^"]+))|({=user}[^"]+))"""
   #"""exa_json_path=$.network_information.source_port,exa_field_name=src_port"""
   #"""exa_json_path=$.new_logon.account_domain,exa_field_name=domain"""
   """exa_json_path=$.log.jsonPayload.message,exa_field_name=additional_info"""
   """exa_json_path=$.log.jsonPayload.ProviderName,exa_field_name=provider_name"""
   #"""exa_json_path=$.logon_information.logon_type,exa_field_name=login_type"""
   """exa_json_path=$.log.jsonPayload.privileges,exa_field_name=privileges"""
 
}
```