#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-delete-fail-516"
Conditions = [
"""EventCode=516"""
"""Message=Internal resources allocated for the queuing of audit messages have been exhausted"""
]
ParserVersion = "v1.0.0"

leef-mssql-login.Fields} [
    """({event_name}Login succeeded)""",
  ]
ParserVersion = "v1.0.0"
},

${MicrosoftParserTemplates.leef-mssql-login}{
  Name = microsoft-mssql-leef-database-login-success-18454
  Conditions = [ """LEEF""", """ 18454 """, """Login succeeded""", """application=MSSQL""" ]
  Fields = ${MicrosoftParserTemplates.leef-mssql-login.Fields} [
    """({event_name}Login succeeded)""",
  ]
ParserVersion = "v1.0.0"
},

{
Name = microsoft-mssql-kv-database-login-success-14
Vendor = "Microsoft"
Product = "MSSQL"
TimeFormat = ["yyyy-MM-dd HH:mm:ss.SSS", "yyyy-MM-dd HH:mm:ss.SS"]
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
  """SessionLoginName ="+(({domain}[^\\"]+?)\\+({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({db_user}[^"]+))"""
  """NTDomainName ="+({domain}[^"]+)"""
  """TextData="+({db_query}.+?)\s*""""
  """EventClass="+({event_code}\d+)"""
  """ApplicationName ="+({app}[^"]+)"""
]
ParserVersion = "v1.0.0"
},

{
Name = "microsoft-nps-xml-endpoint-authentication-success-6272"
Vendor = "Microsoft"
Product = "Microsoft Network Policy Server"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """<EventID>6272</EventID>"""
  """<Message>Network Policy Server granted access to a user"""
]
Fields = [
  """SystemTime='({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)"""
  """<Computer>({host}[\w\-.]+)"""
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  """({event_code}6272)"""
  """'SubjectUserName'>(?:({user_type}host)/)?(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """'SubjectDomainName'>(?:-|({domain}[^\s\<]+))"""
  """'FullyQualifiedSubjectUserName'>(({domain}[^\\]+)\\+)?(?:-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """'NASIdentifier'>(?:-|({location}[\w\-.]+))"""
  """'CallingStationID'>(?:-|({src_mac}[^\<]+))"""
  """'AuthenticationProvider'>(?:-|({auth_server}[^\<]+))"""
  """'FullyQualifiedSubjectMachineName'>(?:-|({user_type}.+?))(\/[^\/\s]+)?<"""
  """'NASIPv6Address'>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """'NASIPv4Address'>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """'EAPType'>(?:-|({auth_type}[^\<]+))"""
  """'QuarantineState'>(?:-|({access_type}[^\<]+))"""
]
ParserVersion = "v1.0.0"
},

{
Name = microsoft-mssql-cef-database-login-fail-24003
Vendor = "Microsoft"
Product = "MSSQL"
TimeFormat = "MMM dd yyyy HH:mm:ss z"
Conditions = [
  """CEF:"""
  """|LOGbinder|SQL|"""
  """|24003|Login failed|"""
]
Fields = [
  """({host}[\w.\-]+)\s+CEF:"""
  """\Wrt=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d \w+)"""
  """\Wsuser=(n/a|(({domain}[^=\\\/]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)"""
  """\WdeviceExternalId=(|({dest_host}[\w\-.]+?))(\s+\w+=|\s*$)"""
  """\Wcs1=({result_reason}[^;\.]+)"""
  """Reason:\s*({result_reason}[^;\.]+)"""
  """<address>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?</address>"""
  """CLIENT:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"
},

{
Name = "microsoft-nps-cef-endpoint-login-success-accessaccept"
Vendor = "Microsoft"
Product = "Microsoft Network Policy Server"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|Microsoft|NPS|"""
  """|Access-Accept|"""
]
Fields = [
  """\srt=({time}\d{13})"""
  """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\sdvchost=({host}[^\s]+)"""
  """\sduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
  """\sdntdom=({domain}[^\s]+)"""
  """\sdestinationZoneURI=({network}.+?)\s+\w+="""
]
ParserVersion = "v1.0.0"
},

${MicrosoftParserTemplates.leef-mssql-login}{
  Name = microsoft-mssql-leef-database-login-fail-18456
  Conditions = [ """LEEF""", """ 18456 """, """Login failed""", """application=MSSQL""" ]
  Fields = ${MicrosoftParserTemplates.leef-mssql-login.Fields} [
    """({event_name}Login failed)""",
    """Reason:\s+({failure_reason}[^.\[]+?)\s*\.\s\["""
  ]
ParserVersion = "v1.0.0"
},

{
Name = microsoft-mssql-kv-database-login-fail-sqlagent
Vendor = "Microsoft"
Product = "MSSQL"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
Conditions = [
  """, instance_name="""
  """, account_name="""
  """, client_name="""
  """, application_name="""
]
Fields = [
  """\sinstance_name="({additional_info}[^"]+)"""
  """\saccount_name="(({domain}[^\\\/"]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*""""
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
Product = "Event Viewer - DHCP-Server"
TimeFormat = "epoch"
Conditions = [
  """|Microsoft|DHCP|"""
  """|Dhcp_Server|"""
]
Fields = [
  """\srt=({time}\d{13})"""
  """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\sdvchost=({host}[^\s]+)"""
  """\sdhost=({dest_host}[\w\-.]+)"""
  """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
DupFields = [
  "dest_host->user"
]
ParserVersion = "v1.0.0"
},

{
  Name = microsoft-nps-csv-endpoint-login-success-13
  Vendor = Microsoft
  Product = Microsoft Network Policy Server 
  TimeFormat = "MM/dd/yyyy,HH:mm:ss"
  Conditions = [ ""","IAS",""", """,13,"""]
  Fields = [
    """"({host}[^\,]+)","IAS""""
    """,({time}\d\d\/\d\d\/\d\d\d\d,\d\d:\d\d:\d\d)""",
    """\d\d:\d\d:\d\d,\d*,"({domain}[^\\]+)\\({user}[\w\.\-\!\#\^\~]{1,40}\$?)",+?,"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?",.+?,"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?","({src_host}[^"]+)"""",
    """"({dest_host}[\w\-.]+)",\d\d\/\d\d\/\d\d\d\d\s"""
  ]
  ParserVersion = v1.0.0
},

{
  Name = microsoft-nps-csv-endpoint-login-success-ias
  Vendor = Microsoft
  Product = Microsoft Network Policy Server
  TimeFormat = "MM/dd/yyyy,HH:mm:ss"
  Conditions = [ ""","IAS",""", """win_nps""" ]
  Fields = [
    """"({host}[^,"]+)","IAS",({time}\d\d\/\d\d\/\d\d\d\d,\d\d:\d\d:\d\d)""",
    """\d\d:\d\d:\d\d,\d*,("host\/({src_host}[^,"]+?)"|[,]*),("({domain}[^\\]+)\\+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"|[^,]*),([^,]*,){8}("({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"|[^,]*),""",
    """(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w.\-]+))\s+\d\d\/\d\d\/\d\d\d\d\s"""
  ]
  ParserVersion = v1.0.0
},

{
  Name = microsoft-nps-csv-endpoint-login-success-ras
  Vendor = Microsoft
  Product = Microsoft Network Policy Server 
  TimeFormat = "MM/dd/yyyy,HH:mm:ss"
  Conditions = [ ""","RAS",""", """win_nps""" ]
  Fields = [
    """"({host}[^,"]+)","RAS",({time}\d\d\/\d\d\/\d\d\d\d,\d\d:\d\d:\d\d)""",
    """\d\d:\d\d:\d\d,\d*,("({domain}[^\\]+)\\+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"|[^,]*),("({src_host}[^,"\\\/]+)[^"]*?({full_name}[^"\\\/]+)"|[,]*),([^,]*,){8}("({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"|[^,]*),""",
    """(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w.\-]+))\s+\d\d\/\d\d\/\d\d\d\d\s"""
  ]
  ParserVersion = v1.0.0
},

{
  Name = microsoft-nps-csv-endpoint-login-success-ias-1
  Vendor = Microsoft
  Product = Microsoft Network Policy Server 
  TimeFormat = "MM/dd/yyyy,HH:mm:ss"
  Conditions = [ ""","IAS",""", """",2,"""" ]
  Fields = [
    """({host}[^"]+)","IAS",({time}\d\d\/\d\d\/\d\d\d\d,\d\d:\d\d:\d\d),(|({result}\d+)),(|"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"),([^,]*,){9}(|"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"),(|"({src_host}[^"]+)"),""",
    """"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?",[^,]*,\s*$""",
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
""""src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""dst_ip":\"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
""""id":\d*({event_code}4726)"""
""""firsttime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""
""""DomainID":"({domain}[^\"]+)"""
""""HostID":"({host}[\w\-.]+)"""
""""UserIDSrc":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
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
"""CallerDomain=\"+({src_domain}[^\"]+)\""""
"""CallerLogonId=\"+\([^,]+,({login_id}[^\)]+)\""""
"""CallerUserName =\"+({src_user}[^\"]+)\""""
"""TargetAccountID=\"+\%\{({user_sid}[^}]+)\}\""""
"""TargetAccountName =\"+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\""""
"""CallerMachineName =\"+({src_host}[^\"]+)\""""
]
DupFields = [
"src_domain->domain"
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
"""Computer="+({dest_host}[\w\-.]+)""""
"""EventID="+({event_code}[^\"]+)""""
"""EventRecordID="+({event_id}[^\"]+)""""
"""SubjectUserName ="+({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
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
"""TIME_GENERATED\s*=\s*({time}\d{10})""",
"""({host}[\w\-.]+) ADAuditPlus""",
"""CALLER_USER_NAME\s*=\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
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