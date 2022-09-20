#### Parser Content
```Java
{
Name = microsoft-defenderatp-json-network-session-fail-devicenetworkevents
Conditions = [
  """"AdvancedHunting-DeviceNetworkEvents""""
  """TimeGenerated"""
  """TenantId"""
]
ParserVersion = "v1.0.0"

leef-mssql-login.Fields} [
    """({event_name}Login succeeded)""",
  ]
ParserVersion = "v1.0.0"
},

${MicrosoftParserTemplates.leef-mssql-login}{
  Name = microsoft-mysql-leef-database-login-success-18454
  Conditions = [ """LEEF""", """ 18454 """, """Login succeeded""", """application=MSSQL""" ]
  Fields = ${MicrosoftParserTemplates.leef-mssql-login.Fields} [
    """({event_name}Login succeeded)""",
  ]
ParserVersion = "v1.0.0"
},

{
Name = microsoft-mysql-kv-database-login-success-14
Vendor = "Microsoft"
Product = "SQL Server"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
Conditions = [
  """HostName ="""
  """DatabaseName ="""
  """SessionLoginName ="""
  """EventClass="14""""
]
Fields = [
  """HostName ="+({host}[^"]+)"""
  """StartTime="+({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d+)"""
  """DatabaseName ="+({db_name}[^"]+)"""
  """SessionLoginName ="+(({domain}[^\\"]+?)\\+({user}[^"]+)|({db_user}[^"]+))"""
  """NTDomainName ="+({domain}[^"]+)"""
  """TextData="+({db_query}.+?)\s*""""
  """EventClass="+({event_code}\d+)"""
  """ApplicationName ="+({app}[^"]+)"""
]
ParserVersion = "v1.0.0"
},

${MicrosoftParserTemplates.microsoft-dns-renew-jp}{
  Name = microsoft-windows-kv-dhcp-session-success-dns
  Product = Windows
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """,DNS の更新要求,""" ]
  ParserVersion = "v1.0.0"
},

${MicrosoftParserTemplates.microsoft-dns-renew-jp}{
  Name = microsoft-windows-kv-dhcp-session-success-dns-1
  Product = Windows
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """,DNS の更新は成功しました,""" ]
  ParserVersion = "v1.0.0"
},

{
Name = "microsoft-nps-xml-endpoint-authentication-success-6272"
Vendor = "Microsoft"
Product = "Network Policy Server"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """<EventID>6272</EventID>"""
  """<Message>Network Policy Server granted access to a user"""
]
Fields = [
  """SystemTime='({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)"""
  """<Computer>({host}[\w\-.]+)"""
  """({event_code}6272)"""
  """'SubjectUserName'>(?:({user_type}host)/)?(({domain}[^\\]+)\\+)?({user}[^<]+)"""
  """'SubjectDomainName'>(?:-|({domain}[^\s\<]+))"""
  """'FullyQualifiedSubjectUserName'>(({domain}[^\\]+)\\+)?(?:-|({user}[^\s\\\<]+))"""
  """'NASIdentifier'>(?:-|({location}[\w\-.]+))"""
  """'CallingStationID'>(?:-|({src_mac}[^\<]+))"""
  """'AuthenticationProvider'>(?:-|({auth_server}[^\<]+))"""
  """'FullyQualifiedSubjectMachineName'>(?:-|({user_type}.+?))(\/[^\/\s]+)?<"""
  """'NASIPv6Address'>({dest_ip}[a-fA-F:\d.]+)"""
  """'NASIPv4Address'>({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """'EAPType'>(?:-|({auth_type}[^\<]+))"""
  """'QuarantineState'>(?:-|({access_type}[^\<]+))"""
]
ParserVersion = "v1.0.0"
},

{
Name = microsoft-mysql-cef-database-login-fail-24003
Vendor = "Microsoft"
Product = "SQL Server"
TimeFormat = "MMM dd yyyy HH:mm:ss z"
Conditions = [
  """CEF:"""
  """|LOGbinder|SQL|"""
  """|24003|Login failed|"""
]
Fields = [
  """({host}[\w.\-]+)\s+CEF:"""
  """\Wrt=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d \w+)"""
  """\Wsuser=(n/a|(({domain}[^=\\\/]+)[\\\/]+)?({user}[^=\\\/]+?))(\s+\w+=|\s*$)"""
  """\WdeviceExternalId=(|({dest_host}.+?))(\s+\w+=|\s*$)"""
  """\Wcs1=({failure_reason}[^;\.]+)"""
  """Reason:\s*({failure_reason}[^;\.]+)"""
  """<address>({src_ip}[a-fA-F\d.:]+)</address>"""
  """CLIENT:\s*({src_ip}[a-fA-F\d.:]+)"""
]
ParserVersion = "v1.0.0"
},

{
Name = "microsoft-nps-cef-endpoint-login-success-accessaccept"
Vendor = "Microsoft"
Product = "Network Policy Server"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|Microsoft|NPS|"""
  """|Access-Accept|"""
]
Fields = [
  """\srt=({time}\d+)"""
  """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\sdvchost=({host}[^\s]+)"""
  """\sduser=({user}.+?)\s+\w+="""
  """\sdntdom=({domain}[^\s]+)"""
  """\sdestinationZoneURI=({network}.+?)\s+\w+="""
]
ParserVersion = "v1.0.0"
},

${MicrosoftParserTemplates.leef-mssql-login}{
  Name = microsoft-mysql-leef-database-login-fail-18456
  Conditions = [ """LEEF""", """ 18456 """, """Login failed""", """application=MSSQL""" ]
  Fields = ${MicrosoftParserTemplates.leef-mssql-login.Fields} [
    """({event_name}Login failed)""",
    """Reason:\s+({failure_reason}[^.\[]+?)\s*\.\s\["""
  ]
ParserVersion = "v1.0.0"
},

{
Name = microsoft-mysql-kv-database-login-fail-sqlagent
Vendor = "Microsoft"
Product = "SQL Server"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
Conditions = [
  """, instance_name="""
  """, account_name="""
  """, client_name="""
  """, application_name="""
]
Fields = [
  """\sinstance_name="({additional_info}[^"]+)"""
  """\saccount_name="(({domain}[^\\\/"]+?)[\\\/]+)?({user}[^\\\/"]+?)\s*""""
  """\sclient_name="({src_host}[^"]+)"""
  """\sapplication_name="({app}[^"]+)"""
  """\sdatabase_name="({db_name}[^"]+)"""
  """\serr_desc="({result}[^"]+)"""
  """\sfirst_login="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+)"""
]
ParserVersion = "v1.0.0"
},

{
Name = "microsoft-windows-cef-dhcp-session-success-dhcpserver"
Vendor = "Microsoft"
Product = "Windows"
TimeFormat = "epoch"
Conditions = [
  """|Microsoft|DHCP|"""
  """|Dhcp_Server|"""
]
Fields = [
  """\srt=({time}\d+)"""
  """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\sdvchost=({host}[^\s]+)"""
  """\sdhost=({dest_host}[^\s]+)"""
  """\sdst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
]
DupFields = [
  "dest_host->user"
]
ParserVersion = "v1.0.0"
},

{
  Name = microsoft-nps-csv-endpoint-login-success-13
  Vendor = Microsoft
  Product = Network Policy Server 
  TimeFormat = "MM/dd/yyyy,HH:mm:ss"
  Conditions = [ ""","IAS",""", """,13,"""]
  Fields = [
    """"({host}[^\,]+)","IAS",({time}\d\d\/\d\d\/\d\d\d\d,\d\d:\d\d:\d\d)""",
    """\d\d:\d\d:\d\d,\d*,"({domain}[^\\]+)\\({user}[^"]+)",+?,"({src_ip}[^"]+)",.+?,"({dest_ip}[^"]+)","({src_host}[^"]+)"""",
    """"({dest_host}[^"]+)",\d\d\/\d\d\/\d\d\d\d\s"""
  ]
  ParserVersion = v1.0.0
},

{
  Name = microsoft-nps-csv-endpoint-login-success-ias
  Vendor = Microsoft
  Product = Network Policy Server
  TimeFormat = "MM/dd/yyyy,HH:mm:ss"
  Conditions = [ ""","IAS",""", """win_nps""" ]
  Fields = [
    """"({host}[^,"]+)","IAS",({time}\d\d\/\d\d\/\d\d\d\d,\d\d:\d\d:\d\d)""",
    """\d\d:\d\d:\d\d,\d*,("host\/({src_host}[^,"]+?)"|[,]*),("({domain}[^\\]+)\\+({user}[^"]+)"|[^,]*),([^,]*,){8}("({src_ip}[a-fA-F\d.:]+)"|[^,]*),""",
    """({dest_host}[\w.\-]+)\s+\d\d\/\d\d\/\d\d\d\d\s"""
  ]
  ParserVersion = v1.0.0
},

{
  Name = microsoft-nps-csv-endpoint-login-success-ras
  Vendor = Microsoft
  Product = Network Policy Server 
  TimeFormat = "MM/dd/yyyy,HH:mm:ss"
  Conditions = [ ""","RAS",""", """win_nps""" ]
  Fields = [
    """"({host}[^,"]+)","RAS",({time}\d\d\/\d\d\/\d\d\d\d,\d\d:\d\d:\d\d)""",
    """\d\d:\d\d:\d\d,\d*,("({domain}[^\\]+)\\+({user}[^"]+)"|[^,]*),("({src_host}[^,"\\\/]+)[^"]*?({full_name}[^"\\\/]+)"|[,]*),([^,]*,){8}("({src_ip}[a-fA-F\d.:]+)"|[^,]*),""",
    """({dest_host}[\w.\-]+)\s+\d\d\/\d\d\/\d\d\d\d\s"""
  ]
  ParserVersion = v1.0.0
},

{
  Name = microsoft-nps-csv-endpoint-login-success-ias-1
  Vendor = Microsoft
  Product = Network Policy Server 
  TimeFormat = "MM/dd/yyyy,HH:mm:ss"
  Conditions = [ ""","IAS",""", """",2,"""" ]
  Fields = [
    """({host}[^"]+)","IAS",({time}\d\d\/\d\d\/\d\d\d\d,\d\d:\d\d:\d\d),(|({action}\d+)),(|"({user}[^"]+)"),([^,]*,){9}(|"({src_ip}[^"]+)"),(|"({src_host}[^"]+)"),""",
    """"({dest_ip}[^"]+)",[^,]*,\s*$""",
  ]
  ParserVersion = v1.0.0
},

{
Name = "microsoft-evsecurity-json-user-delete-fail-deleted"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""McAfee_SIEM:"""
"""A user account was deleted."""
]
Fields = [
"""({event_name}A user account was deleted)"""
""""src_ip":"({src_ip}[^\"]+)"""
""""dst_ip":\"({dest_ip}[^\"]+)"""
""""id":\d*({event_code}4726)"""
""""firsttime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""
""""DomainID":"({domain}[^\"]+)"""
""""HostID":"({host}[^\"]+)"""
""""UserIDSrc":"({user}[^\"]+)"""
""""Security_ID":"({user_sid}[^\"]+)"""
""""Source_Logon_ID":"({login_id}[^\"]+)"""
""""UserIDDst":"({dest_user}[^\"]+)"""
]
DupFields = [
"host->dest_host"
"dest_user->account_name"
]
ParserVersion = "v1.0.0"
},

{
Name = "microsoft-evsecurity-kv-user-delete-fail-644"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""LogType="WLS""""
"""EventID="644""""
]
Fields = [
"""EventID=\"+({event_code}[^\"]+)\""""
"""EventRecordID=\"+({event_id}[^\"]+)\""""
"""CallerDomain=\"+({caller_domain}[^\"]+)\""""
"""CallerLogonId=\"+\([^,]+,({login_id}[^\)]+)\""""
"""CallerUserName =\"+({caller_user}[^\"]+)\""""
"""TargetAccountID=\"+\%\{({user_sid}[^}]+)\}\""""
"""TargetAccountName =\"+({user}[^\"]+)\""""
"""CallerMachineName =\"+({src_host}[^\"]+)\""""
]
DupFields = [
"host->dest_host"
"caller_domain->domain"
]
ParserVersion = "v1.0.0"
},

{
Name = "microsoft-evsecurity-kv-user-delete-fail-wls"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""LogType="WLS""""
"""EventID="4726""""
]
Fields = [
"""Computer="+({dest_host}[^\"]+)""""
"""EventID="+({event_code}[^\"]+)""""
"""EventRecordID="+({event_id}[^\"]+)""""
"""SubjectUserName ="+({user}[^\"]+)""""
"""SubjectDomainName ="+({domain}[^\"]+)""""
"""SubjectLogonId="+({login_id}[^\"]+)""""
"""SubjectUserSid="+({user_sid}[^\"]+)""""
"""TargetDomainName ="+({dest_domain}[^\"]+)""""
"""TargetUserName ="+({dest_user}[^\"]+)""""
"""TargetSid="+({dest_user_sid}[^\"]+)""""
]
DupFields = [
"dest_user->account_name"
]
ParserVersion = "v1.0.0"
},

{
Name = microsoft-evsecurity-kv-user-delete-fail-deleted
Vendor = Microsoft
Product = Event Viewer - Security
ParserVersion = "v1.0.0"
TimeFormat = "epoch_sec"
Conditions = [ """ADAuditPlus""", """EVENT_NUMBER = 4726""", """A user     account was deleted""" ]
Fields = [
"""TIME_GENERATED\s*=\s*({time}\d+)""",
"""({host}[\w\-.]+) ADAuditPlus""",
"""CALLER_USER_NAME\s*=\s*({user}[^\s\]]+)""",
"""CALLER_USER_DOMAIN\s*=\s*({domain}[^\s\]]+)""",
"""SOURCE\s*=\s*({src_host}[\w\-.]+)""",
"""RECORD_NUMBER\s*=\s*({event_id}\d+)""",
"""EVENT_NUMBER\s*=\s*({event_code}\d+)""",
"""CALLER_USER_SID\s*=\s*({user_sid}[^\s]+)""",
"""CALLER_LOGON_ID\s*=\s*({login_id}[^\s]+)""",
"""ACCOUNT_NAME\s*=\s*({dest_user}[^\s]+)""",
"""ACCOUNT_DOMAIN\s*=\s*({dest_domain}[^\]]+?)\s*\]""",
"""ACCOUNT_SID\s*=\s*\%\{({dest_user_sid}[^\s\}]+)""",
]
DupFields=[ "host->dest_host", "dest_user->account_name" 
}
```