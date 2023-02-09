#### Parser Content
```Java
{
Name = microsoft-windows-kv-scheduled-task-finish-success-201
  ParserVersion = "v1.0.0"
  Conditions = [ """eventid="201"""", """Microsoft-Windows-TaskScheduler""" ]
  Fields = ${WindowsParsersTemplates.windows-events-2.Fields}[
    """({event_name}Task Scheduler successfully completed task)""",
  ]

windows-events-2 = {
 Vendor = Microsoft
 Product = Windows
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
 Fields = [
   """timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
   """"EventID"+:"+({event_code}\d+)""",
   """"subject.logon_id"+:"+({login_id}[^"]+)""",
   """"subject.security_id"+:"+({user_sid}[^"]+)""",
   """"process_information.process_name"+:"+({process_path}({process_dir}[^"]*)\\\\({process_name}[^"]+))""",
   """"process_information.process_id"+:"+({process_id}[^"]+)""",
   """"Computer"+:"+({host}[^"]+)""",
   """"subject.account_name"+:"+(-|({email_address}({user}[^@]+)@({domain}[^"]+))|({=user}[^"]+))""",
   """"network_information.source_port"+:"+(-|({src_port}\d+))""",
   """"new_logon.account_domain"+:"+({domain}[^"]+)""",
   """"message"+:"+({additional_info}[^"]+)""",
   """"ProviderName"+:"+({provider_name}[^"]+)""",
   """"logon_information.logon_type"+:"+({login_type}\d+)"""
 
}
```