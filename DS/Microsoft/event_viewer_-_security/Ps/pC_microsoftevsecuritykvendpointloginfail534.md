#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-fail-534"
Conditions = [
  """LogType="WLS""""
  """EventID="534""""
]
ParserVersion = "v1.0.0"

netapp-json-windows-events-1.Fields}[
    """'Computer':\s+'({host}[\w\-\.]+)""",
  ]
  DupFields = [ "access->event_name","object_class->file_type" ]
  ParserVersion = "v1.0.0"
},

{
Name = "microsoft-evsecurity-cef-endpoint-login-success-540"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
"""|Microsoft|Microsoft Windows|"""
"""|Security:540|"""
]
Fields = [
"""({event_name}Successful Network Logon)"""
"""({event_code}540)"""
"""\srt=({time}\d{13})"""
"""\ssproc=({auth_process}.+?)\s+\w+="""
"""\sduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
"""\sduid=\([^,]+,({login_id}[^\)]+)"""
"""\scn1=({login_type}\d+)"""
"""\sdvchost=({host}[^\s]+)"""
""" dntdom=({domain}[^\s]+)"""
""" src=(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s+\w+="""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"
},

{
Name = "microsoft-evsecurity-cef-user-create-success-624"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
"""|Microsoft|Microsoft Windows|"""
"""|Security:624|"""
]
Fields = [
"""({event_name}User Account Created)"""
"""({event_code}624)"""
"""\srt=({time}\d{13})"""
"""\ssntdom=({domain}[^\s]+)"""
"""\ssuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
"""\ssuid=\([^,]+,({login_id}[^\)]+)"""
"""\sdntdom=({account_domain}.+?)\s+\w+="""
"""\sduser=({account_name}.+?)\s+\w+="""
"""\sdvchost=({host}[^\s]+)"""
"""\sduser=(({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)|({dest_user_full_name}.+?))\s+\w+="""
]
ParserVersion = "v1.0.0"
},
{
  Name = microsoft-evsecurity-json-alert-trigger-success-4649
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  ExtractionType = json
  Conditions = [ """"EventID":4649""", """"Message":"A replay attack was detected""", """Microsoft-Windows-Security-Auditing""", """"Channel":"Security"""" ]
  Fields = [
  """exa_json_path=$.EventTime,exa_field_name=time""",
  """exa_json_path=$.EventID,exa_field_name=event_code""",
  """exa_json_path=$.Hostname,exa_field_name=host""",
  """exa_json_path=$.Computer,exa_field_name=host"""
  """exa_json_path=$.Channel,exa_field_name=channel""",
  """exa_json_path=$.Message,exa_regex=({event_name}[^\.]+).\s*Subject""",
  """exa_json_path=$.EventType,exa_field_name=event_category""",
  """exa_json_path=$.SeverityValue,exa_field_name=alert_severity""",
  """exa_json_path=$.SourceName,exa_field_name=app""",
  """exa_json_path=$.ProviderGuid,exa_field_name=process_guid""",
  """exa_json_path=$.Task,exa_field_name=task_name""",
  """exa_json_path=$.OpcodeValue,exa_field_name=opcode""",
  """exa_json_path=$.RecordNumber,exa_field_name=event_id""",
  """exa_json_path=$.ActivityID,exa_field_name=activity_id""",
  """exa_json_path=$.ProcessID,exa_field_name=process_id""",
  """exa_json_path=$.ThreadID,exa_field_name=thread_id""",
  """exa_json_path=$.Category,exa_field_name=category""",
  """exa_json_path=$..SubjectUserSid,exa_field_name=user_sid""",
  """exa_json_path=$..SubjectUserName,exa_regex=^({user}[\w\.\-\!\#\^\~]{1,40}\$?)$""",
  """exa_json_path=$..SubjectDomainName,exa_field_name=domain""",
  """exa_json_path=$..SubjectLogonId,exa_field_name=login_id""",
  """exa_json_path=$.TargetUserName,exa_field_name=dest_user"""
  """exa_json_path=$.TargetDomainName,exa_field_name=dest_domain"""
  """exa_json_path=$.RequestType,exa_field_name=dns_query_type"""
  """exa_json_path=$..LogonProcessName,exa_regex=^(-|({auth_process}.+?))\s*$""",
  """exa_json_path=$.AuthenticationPackage,exa_field_name=auth_package"""
  """exa_json_path=$..ProcessName,exa_regex=^({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))$""",
  """exa_json_path=$..WorkstationName,exa_field_name=src_host_windows,exa_match_expr=!InList($.WORKSTATION_NAME,"-")"""
  """exa_regex=Subject: Security ID:\s*({user_sid}S-[^\s]+)\s*Account Name: ({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*Account Domain:\s*({domain}[^\s]+)\s* Logon ID:\s*({login_id}[^\s]+)"""
  """exa_regex=Process Name:\s+({process_path}(({process_dir}[^\s]+)\\+)?({process_name}[^\s]+))\s+Network Information:"""
  """exa_regex=Authentication Package:\s+({auth_package}[^\s]+)""",
  """exa_regex=Logon Process:\s+({auth_process}[^\s]+)"""
  ]
  DupFields = [ "event_name->alert_name", "auth_process->alert_type", "user->src_user", "domain->src_domain" ]
  ParserVersion = "v1.0.0"
}

{
  Name = microsoft-evsecurity-kv-alert-trigger-success-4649
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = [ """EventCode=4649""", """Message=A replay attack was detected.""", """SourceName =Microsoft Windows security auditing""", """TaskCategory=Other Logon/Logoff Events""" ]
  Fields = [
    """({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(AM|PM))""",
    """EventCode=({event_code}\d+)""",
    """ComputerName =({host}[^\s]+)""",
    """Keywords=({result}[^=]+?)\s+\w+=""",
    """Message=({event_name}[^:]+?)\s+\w+:""",
    """Subject:\s+Security ID:\s+({user_sid}[^:]+?)\s+Account Name:""",
    """Subject:.+?Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """Subject:.+?Account Domain:\s+({domain}[^:]+?)\s+Logon ID:""",
    """Subject:.+?Logon ID:\s+({login_id}[^\s]+)""",
    """Process ID:\s+({process_id}[^\s]+)""",
    """Process Name:\s+({process_path}(({process_dir}[^\s]+)\\+)?({process_name}[^\s]+))\s+Network Information:""",
    """Logon Process:\s+({auth_process}[^\s]+)""",
    """Authentication Package:\s+({auth_package}[^\s]+)""",
    """({additional_info}This event indicates that[^$]+?)\s*$"""
  ]
  DupFields = [ "event_name->alert_name", "auth_process->alert_type" ]
  ParserVersion = "v1.0.0"
},

{
    Name = microsoft-evsecurity-kv-process-create-success-4688-3
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSZ"
    Conditions = [ """Exabeam Windows 4688""", """summary_windows_4688_data""" ]
    Fields = [
      """search_time=({time}\d+)"""
      """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+[+-]\d+)""",
      """({event_code}4688)""",
      """summary_windows_4688_data="+\d+:\d+:\d+\s*\d+-\d+-\d+:::({host}[^:::]+)?:::({user_sid}[^:::]+)?:::({user}[\w\.\-\!\#\^\~]{1,40}\$?)?:::({domain}[^:::]+)?:::({login_id}[^:::]+)?:::({process_guid}[^:::]+)?:::({process_path}({process_dir}(?:.+?)?[\\\/])?({process_name}[^\\\/:::]+))?:::({process_command_line}[^:::]+)?:::({parent_process_guid}[^:::]+)?:::({operation_type}[^:::]+)?""""
    ]
    DupFields = [ "process_guid->process_id" , "host->src_host" ]
	ParserVersion = "v1.0.0"
  },

{
  Name = microsoft-windows-kv-process-create-success-processid
  Vendor = Microsoft
  Product = Microsoft WMI Log
  TimeFormat = "yyyyMMddHHmmss.SSSSSS"
  Conditions = [ """ProcessName ="""", """ProcessId=""", """CommandLine="""" ]
  Fields = [
    """StartTime="({time}\d+\.\d+)""",
    """Host="({host}[^"]+)""",
    """ProcessId=({process_guid}.+?)\s+(\w+=|$)""",
    """CommandLine="*({process_command_line}[^"]+?)\s*"""",
    """Path="({path}[^"]+)""",
    """Path="({process_path}({process_dir}[^"]+?)({process_name}[^"\\]+))"""",
    """ProcessName ="({process_name}[^"]+)""",
  ]
  DupFields = [ "host->dest_host", "process_guid->process_id" ]
  ParserVersion = "v1.0.0"
},

{
  Name = microsoft-evsecurity-kv-process-create-success-4688-4
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = ["""Se creó un nuevo proceso""", """Dominio de cuenta:""", """EventCode=4688"""]
  Fields = [
   """Message=({event_name}Se creó un nuevo proceso)""",
   """({event_code}4688)""",
   """\s({host}[^\s]+)\s({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(?i)(AM|PM))""",
   """({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(?i)(AM|PM))"""
   """Firmante creador:\s*Identificador de seguridad:\s*({user_sid}[^\s]+)\s*Nombre de cuenta:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*Dominio de cuenta:\s*({domain}[^\s]+)\s*Identificador de inicio de sesión:\s*({login_id}[^\s]+)""",
   """Nombre del nuevo proceso:\s*(?:|({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/\s]+)))\s+Tipo de elevación de token:""",
  ]
  ParserVersion = "v1.0.0"
},

{
  Name = microsoft-evpowershell-cef-process-create-success-300
  Vendor = Microsoft
  Product = Event Viewer - PowerShell
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "epoch"]
  Conditions = [ """CEF: """, """|Microsoft|PowerShell|""", """PowerShell:300|""" ]
  Fields = [
    """\Wrt=({time}\d{13})""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"UserId"":""({user_sid}.+?)"""",
    """"Computer"":""({host}.+?)"""",
    """"ScriptBlockId"":""({scriptblock_id}.+?)"""",
    """"ScriptBlockText"":""({scriptblock_text}.+?)"""",
    """-Function\s+'({function}[^']+)""",
    """"MessageTotal"":""(|({message_total}.+?))"""",
    """"MessageNumber"":""(|({message_number}.+?))"""",
    """message=({script_message}[^:]+)""",
    """"Path"":""(|({path}.+?))"""",
    """"ProcessID"":""({process_id}\d+)"""",
    """-file\s({process_path}({process_dir}[^\s]+\\\\({process_name}[^\s\\]+)))""",
    """CommandLine\\*=({process_command_line}[^\s]+)""",
  ]
  ParserVersion = "v1.0.0"
},

{
  Name = microsoft-evpowershell-cef-process-create-success-4102
  Vendor = Microsoft
  Product = Event Viewer - PowerShell
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """CEF: """, """|Microsoft|PowerShell|""", """|Microsoft-Windows-PowerShell:4102|""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """\sduser=(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s""",
    """\sahost=({host}[^\s]+)\s""",
    """\sad.ProcessID=({process_id}[^\s]+)\s""",
    """\|Microsoft-Windows-PowerShell:4102\|({additional_info}[^|]+)\|""",
  ]
  ParserVersion = "v1.0.0"
},

{
  Name = microsoft-evsecurity-cef-process-create-success-4688-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "epoch"
  Conditions = [ """|Microsoft-Windows-Security-Auditing:4688|""", """|Snare|""" ]
  Fields = [
    """({event_name}A new process has been created)""",
    """\Wrt=({time}\d{13})""",
    """\Wdhost=({host}[\w\-\.]+)\s*(\w+=|$)""",
    """\Wdvchost=({host}[\w\-\.]+)\s*(\w+=|$)""",
    """\Wdst=({dest_ip}[a-fA-F:\.\d]+)\s*(\w+=|$)""",
    """({event_code}4688)""",
    """\Wduser=(?:-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*(\w+=|$)""",
    """\Wdntdom=(?:-|({domain}[^\s]+))\s*(\w+=|$)""",
    """\WdeviceNtDomain=(?:-|({domain}[^\s]+))\s*(\w+=|$)""",
    """\Wdproc=({process_path}({process_dir}(?:[^"]+?)?[\\\/])?({process_name}[^\\\/]+?))\s*(\w+=|$)""",
    """\Wdproc=({path}.+?)\s*(\w+=|$)""",
    """\Wduid=({login_id}[^\s]+)\s*(\w+=|$)""",
    """\Wcs2=({operation_type}.+?)\s*(\w+=|$)""",
    """\Wcs3=({process_guid}[^\s]+)\s*(\w+=|$)""",
    """\Wcs4=({process_command_line}.+?)\s*(\w+=|$)""",
    """\Wcs5=({parent_process_guid}[^\s]+)\s*(\w+=|$)""",
  ]
  DupFields = [ "process_guid->process_id" , "host->src_host" ]
  ParserVersion = "v1.0.0"
},

{
  Name = microsoft-windows-cef-process-create-success-snare
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Snare|""", """|A new process has been created|""" ]
  Fields = [
    """\srt=({time}\d{13})""",
    """CEF:([^\|]*\|){4}Security:({event_code}\d+)\|({event_name}[^\|]+)""",
    """\scategoryBehavior=(|({action}.+?))(\s+\w+=|\s*$)""",
    """\scategoryOutcome=(|/({result}.+?))(\s+\w+=|\s*$)""",
    """\scategoryObject=(|({object}.+?))(\s+\w+=|\s*$)""",
    """\sdhost=(|({dest_host}[\w\-.]+?))(\s+\w+=|\s*$)""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sduser=(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)""",
    """\sdproc=(|({process_path}(({process_dir}[^=]*?)[\\\/]+)?({process_name}[^=\\\/]+)))(\s+\w+=|\s*$)""",
    """Process ID\\=({process_id}\d+)""",
    """User\\=(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """ComputerName\\=({host}[\w.\-]+)""",
  ]
  ParserVersion = "v1.0.0"
},

{
  Name = microsoft-evpowershell-kv-process-create-success-4104-1
  Vendor = Microsoft
  Product = Event Viewer - PowerShell
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """eventid="4104"""", """Microsoft-Windows-PowerShell""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d+Z\s*({host}[^\s]+)\s""",
    """eventid="+({event_code}\d+)""",
    """providername="+({provider_name}[^"]+)""",
    """userid="(?:[^\\]+\\+)?(SYSTEM|NETWORK SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """\stask="+({operation}[^"]+)""",
    """\Weventrecordid="+({event_id}\d+)"""",
    """({event_name}Creating Scriptblock text)""",
    """ScriptBlock ID:\s+({scriptblock_id}[^\s]+)""",
    """({process_name}PowerShell)""",
    """Creating Scriptblock text\s*\([^\)]+\):\s*({scriptblock_text}.+?)\s*ScriptBlock ID:""",
  ]
  DupFields = ["event_id->event_code"]
  ParserVersion = "v1.0.0"
},

{
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Fields = [
  """({time}\d+-\d+-\d+T\d+:\d+:\d+).+\sLogType"""
  """EventID="+({event_code}\d+)""""
  """Opcode.+ProcessName ="+(-|({process_path}({process_dir}(:?[\w:]+)?[^.]+[\\\/]+))({process_name}[^"]+))""""
  """ServiceName ="+({service_name}[^"]+)""""
  """ServiceType="+({service_type}[^"]+)""""
  """ServiceAccount="+({account_name}[^"]+)""""
  """SubjectUserName ="+(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
  """SubjectDomainName ="+(-|({domain}[^"]+))""""
  """SubjectLogonId="+({login_id}[^"]+)""""
  """ProviderGuid="+({process_guid}[^"]+)""""
  """CommandLine="+({process_command_line}[^"]+)""""
  """SubjectUserSid="+({user_sid}[^"]+)""""
  """SubjectUserName ="+(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
  """ObjectServer="+({object_server}[^"]+)""""
  """ProcessId="+({process_id}[^"]+)""""
  """Computer="+({dest_host}[\w\-.]+)""""
  """TargetDomainName ="+(-|({dest_domain}[^"]+))""""
  """TargetUserName ="+(-|({dest_user}[^"]+))""""
  """TargetLogonId="+({dest_user_sid}[^"]+)""""
  """TargetUserSid="+({dest_user_sid}[^"]+)""""
  """ExecutionProcessID="+({process_id}d+)""""
  """FailureReason="+({failure_reason}[^"]+)""""
  """WorkstationName ="+(-|({client}[^"]+))""""
  """MemberName ="+({user_dn}[^"]+)""""
  """MemberSid="+({account_id}[^"]+)""""
  """LogonType="+({login_type}\d+)""""
  """SubStatus="+({result_code}[^"]+)""""
  """LogonProcessName ="({auth_process}[^"]+)""""
  """KeyLength="({key_length}\d+)""""
  """AuthenticationPackageName ="({auth_package}[^"]+)""""
  """IpAddress="(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""""
]
DupFields = [ "dest_host->host", "user->src_user", "domain->src_domain" ]
Name = "microsoft-evsecurity-kv-endpoint-login-fail-534"
Conditions = [
  """LogType="WLS""""
  """EventID="534""""
]
ParserVersion = "v1.0.0"
},

{
    Name = microsoft-windows-xml-endpoint-login-fail-4825
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = ["""<EventID>4825</EventID>""", """<Provider>Microsoft Windows security auditing.</Provider>""", """<Message>A user was denied the access to Remote Desktop."""]
    Fields = [
      """TimeCreated SystemTime(\\)?=('|")({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
      """<Computer>({host}({dest_host}[\w\-\.]+))</Computer>""",
      """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
      """<EventID>({event_code}\d+)</EventID>""",
      """<Data Name(\\)?=('|")AccountName('|")>(?=\w)?(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<\/Data>""",
      """<Data Name(\\)?=('|")AccountDomain('|")>(-|({domain}[^<]+))<\/Data>""",
      """<Data Name(\\)?=('|")LogonID('|")>({login_id}\w+)<\/Data>""",
      """<Data Name(\\)?=('|")ClientAddress('|")>({src_ip}[a-fA-F0-9\.:]+)<\/Data>""",
      """<Message>({event_name}A user was denied the access to Remote Desktop).""",
      """<Level>({run_level}[^<]+)<"""
    ]
    ParserVersion = "v1.0.0"
  },

  {
    Name = microsoft-windows-xml-endpoint-login-fail-4825-1
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = ["""<EventID>4825</EventID>""", """Microsoft-Windows-Security-Auditing""" ]
    Fields = [
      """TimeCreated SystemTime(\\)?=('|")({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
      """<Computer>({host}({dest_host}[\w\-\.]+))</Computer>""",
      """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
      """<EventID>({event_code}\d+)</EventID>""",
      """<Data Name(\\)?=('|")AccountName('|")>(?=\w)?(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<\/Data>""",
      """<Data Name(\\)?=('|")AccountDomain('|")>(-|({domain}[^<]+))<\/Data>""",
      """<Data Name(\\)?=('|")LogonID('|")>({login_id}\w+)<\/Data>""",
      """<Data Name(\\)?=('|")ClientAddress('|")>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))<\/Data>""",
      """<Message>({event_name}A user was denied the access to Remote Desktop).""",
      """<Level>({run_level}[^<]+)<"""
    ]
    ParserVersion = "v1.0.0"
  },

  {
    Name = microsoft-windows-kv-endpoint-login-fail-4825
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = "MM/dd/yyyy hh:mm:ss a"
    Conditions = ["""EventCode=4825""", """Microsoft Windows security auditing.""", """A user was denied the access to Remote Desktop."""]
    Fields = [
      """({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(am|AM|pm|PM))""",
      """EventCode=({event_code}\d+)\s*""",
      """User Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Domain:\s+({domain}.+?)\s+Logon ID:\s+({login_id}[^\s]+)\s+""",
      """Client Address:\s+(::[\w]+:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """Message=({event_name}A user was denied the access to Remote Desktop).""",
      """ComputerName =({host}[\w.\-]+)"""
      """RecordNumber=({event_id}\w+)"""
      """LogName =({log_name}[^\s]+)"""
    ]
    ParserVersion = "v1.0.0"
  },

{
Name = microsoft-evsecurity-cef-user-switch-success-4648-1
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
  """|Snare|"""
  """|Microsoft-Windows-Security-Auditing:4648|"""
]
Fields = [
  """({event_name}A logon was attempted using explicit credentials)"""
  """\sexternalId=({event_code}\d+)"""
  """\srt=({time}\d{13})"""
  """\sdvc=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\sdvchost=({dest_host}[\w\-.]+)"""
  """\sduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
  """\ssuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
  """\sduser=({account}.+?)\s+\w+="""
  """\sdntdom=({domain}[^\s]+)"""
  """\sduid=({login_id}[^\s]+)"""
  """dproc=(?: |({process_path}({process_dir}(?:[^=]+)?[\\\/])?({process_name}[^\\\/=]+)))\s+\w+="""
  """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
DupFields = [
  "dest_ip->host"
]
ParserVersion = "v1.0.0"
},

{
Name = microsoft-evsecurity-cef-user-switch-success-552
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
  """|Snare|"""
  """|Security:552|Logon attempt using explicit credentials|"""
]
Fields = [
  """({event_name}Logon attempt using explicit credentials)"""
  """({event_code}552)"""
  """\srt=({time}\d{13})"""
  """ahost=({host}[^\s]+)"""
  """dvchost=({dest_host}[\w\-.]+)"""
  """duser=({account}[\w\-\.]+(?:\w+)?\$?)\s+\w+="""
  """suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
  """dntdom=({domain}.+?)\s+\w+="""
  """OriginalAgentAddress=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """dvc=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
ParserVersion = "v1.0.0"
},

{
Name = "microsoft-evsecurity-cef-endpoint-672"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
  """|Microsoft|Microsoft Windows|"""
  """|Security:672|"""
]
Fields = [
  """({event_name}Account Logon)"""
  """({event_code}672)"""
  """\srt=({time}\d{13})"""
  """src=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\ssuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
  """\scs4=({result_code}[^\s]+)"""
  """\sdvchost=({host}[^\s]+)"""
  """\sdntdom=({domain}[^\s]+)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"
},

{
Name = "microsoft-evsecurity-kv-success-esm"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
  """|McAfee|ESM"""
  """43-21100552"""
]
Fields = [
  """({event_name}Logon attempt using explicit credentials)"""
  """\|McAfee\|[^|]+?\|[^|]+?\|43-21100({event_code}\d+)(0|1)\|"""
  """rt=({time}\d{13})"""
  """deviceTranslatedAddress=({host}[a-fA-F:\d.]+)"""
  """shost=({dest_host}[\w\-.]+)"""
  """duser=({dest_user}[\w\-\.]+(?:\w+)?\$?)\s+suser"""
  """suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+nitroSource"""
  """sntdom=({domain}.+?)\s+shost"""
  """nitroSource_Logon_ID=\([^,]+,({login_id}[^\)]+)"""
]
ParserVersion = "v1.0.0"
},

{
Name = "microsoft-windows-kv-endpoint-login-esm"
Vendor = "Trellix"
Product = "Trellix Enterprise Security Manager"
TimeFormat = "epoch"
Conditions = [
  "|McAfee|ESM"
  "43-21100680"
]
Fields = [
  """\|McAfee\|[^|]+?\|[^|]+?\|43-21100({event_code}\d+)(0|1)\|"""
  """({event_name}Logon attempt)"""
  """\srt=({time}\d{13})"""
  """src=({host}[a-fA-F:\d.]+)"""
  """nitroCommandID=({result_code}.+?)\s+\w+="""
  """sntdom=({domain}[^\s]+)"""
  """suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
  """shost=({dest_host}[\w\-.]+?)\s+\w+="""
]
ParserVersion = "v1.0.0"
},

{
Name = "microsoft-windows-kv-endpoint-login-fail-failure"
Vendor = "Trellix"
Product = "Trellix Enterprise Security Manager"
TimeFormat = "epoch"
Conditions = [
  """|McAfee|ESM"""
  """43-211005"""
  """failure"""
]
Fields = [
  """({event_name}Logon Failure)"""
  """\|McAfee\|[^|]+?\|[^|]+?\|43-21100({event_code}\d+)(0|1)\|"""
  """\srt=({time}\d{13})"""
  """deviceTranslatedAddress=({host}[a-fA-F:\d.]+)"""
  """sntdom=({domain}[^\s]+)"""
  """nitroLogon_Type=({login_type}\d+)"""
  """nitroAppID=({auth_package}[^\s]+)"""
  """suser=({src_user}.+?)\s+\w+="""
  """suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
  """duser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
  """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """nitroSource_Logon_ID=\([^,]+,({login_id}[^\)]+)"""
  """nitroDestination_Logon_ID=({login_id}\d+)"""
]
DupFields = [
  "host->dest_host"
  "event_code->result_code"
]
ParserVersion = "v1.0.0"
},

{
Name = "microsoft-evsecurity-cef-endpoint-login-680"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """|Snare|"""
  """|Security:680|"""
]
Fields = [
  """({event_code}680)"""
  """({event_name}Logon attempt)"""
  """\srt=({time}\d+)"""
  """ahost=({host}[^\s]+)"""
  """suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
  """dhost=({dest_host}[\w\-.]+?)\s+\w+="""
]
ParserVersion = "v1.0.0"
},

{
Name = "microsoft-evsecurity-kv-endpoint-login-680-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
  """(680)"""
  """Logon attempt by:"""
]
Fields = [
  """({event_name}Logon attempt)"""
  """({time}\w+ \d{1,2} [\d:]+ \d+):"""
  """\d{4}:[\s/]([^/]+)\/Security"""
  """/Security \(({event_code}680)\)"""
  """Logon account:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)(?:@({domain}[^\s.]+)[^\s]*)?\s+Source Workstation:\s+({dest_host}[\w\-.]+)"""
  """Error Code:\s+({result_code}[^\s]+)"""
]
ParserVersion = "v1.0.0"
},

{
Name = "microsoft-evsecurity-kv-endpoint-login-680-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyyMMddHHmmss.SSS"
Conditions = [
  """EventCode = 680;"""
  """Logon attempt by:"""
]
Fields = [
  """Computer(Name)? = "+({host}[^"]+)""""
  """({event_name}Logon attempt)"""
  """EventCode = ({event_code}\d+)"""
  """TimeGenerated = "({time}[\d]+.\d\d\d)"""
  """Logon account:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)(?:@({domain}[^\s.]+)[^\s]*)?\s+Source Workstation:\s+({dest_host}[\w\-.]+)"""
  """Error Code:\s+({result_code}[\w\-]+)"""
]
ParserVersion = "v1.0.0"
},

{
Name = "microsoft-evsecurity-kv-endpoint-login-672-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy hh:mm:ss a"
Conditions = [
  """EventCode=672"""
  """Service Name:"""
  """krbtgt"""
]
Fields = [
  """({event_name}Account Logon)"""
  """ComputerName =({host}[\w.\-]+)"""
  """EventCode=({event_code}\w+)"""
  """User Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Supplied Realm Name:\s+({domain}[^\s]+)"""
  """Client Address:\s+(::[\w]+:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """Result Code:\s+({result_code}[\w\-]+)"""
  """Sid=({user_sid}[^\s]+)\s+SidType"""
]
ParserVersion = "v1.0.0"
},

${WindowsParsersTemplates.windows-events-wls} {
  Name = microsoft-evsecurity-kv-endpoint-login-success-4648-4
  Conditions = [ """LogType="WLS"""", """EventID="4648"""" ]
  ParserVersion = "v1.0.0"
  Fields = ${WindowsParsersTemplates.windows-events-wls.Fields}[
    """Computer="+({host}[\w\-.]+)""""
  ]
  DupFields = [ "host->dest_host", "user->src_user", "domain->src_domain" ]
 },

${WindowsParsersTemplates.windows-events-wls} {
  Name = microsoft-evsecurity-kv-endpoint-login-success-552
  Product = "Event Viewer - Security"
  Conditions = [ """LogType="WLS"""", """EventID="552"""" ]
  ParserVersion = "v1.0.0"
  Fields = ${WindowsParsersTemplates.windows-events-wls.Fields}[
    """Computer="+({host}[\w\-.]+)""""
  ]
  DupFields = [ "host->dest_host", "user->src_user", "domain->src_domain" 
}
```