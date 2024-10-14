#### Parser Content
```Java
{
Name = "beyondtrust-prividentity-cef-app-activity-accountdeelevated"
Conditions = [
  """CEF:"""
  """|Liebsoft|"""
  """|EVENT_ID_JOB_ACCOUNT_ELEVATION_DEELEVATED|"""
]
ParserVersion = "v1.0.0"

json-beyondtrust-activity-1.Fields}[
    """exa_json_path=$.Arguments,exa_field_name=process_command_line""",
    """exa_json_path=$.EventDesc,exa_field_name=event_name""",
    ]
	ParserVersion = "v1.0.0"
},

{
  Name = beyondtrust-powerbroker-str-process-create-success-messageforwarded
  Vendor = BeyondTrust
  Product = BeyondInsight
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ Message forwarded from """, """: accepted """ ]
  Fields = [
    """\s+Message forwarded from ({host}[\w\-.]+)""",
    """accepted ({process_path}({process_dir}.+?[\\\/])?({process_name}[^\\\/]+?)) from ({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({src_host}[\w\-.]+) to ({account}[^\s@]+)@({dest_host}[\w\-.]+)""",
  ]
  ParserVersion = "v1.0.0"
},

{
Name = "beyondtrust-passwordsafe-kv-user-passwordretrieve"
Vendor = "BeyondTrust"
Product = "BeyondInsight"
TimeFormat = "MM/dd/yyyy HH:mm:ss"
Conditions = [
"""Event Desc: Password Retrieve"""
"""Agent ID: PBPS"""
"""Failed: False"""
]
Fields = [
"""LogTime:\s*({time}\d+\/\d+\/\d+ \d+:\d+:\d+)"""
"""User:\s*(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+\s)?\w+:"""
"""Source Host:\s*({host}[^\s]+)"""
"""Event Subject:\s*0*({src_ip_1}\d+\.)0*({src_ip_2}\d+\.)0*({src_ip_3}\d+\.)0*({src_ip_4}\d+)"""
"""Target:.*?Asset:({dest_host}[^\s]+)\s+\w+:"""
"""Target:.*?MAccount:({dest_user}[^\s]+)\s+\w+:"""
"""RoleUsed:\s*({privileges}.+?)\s+\w+:"""
"""Agent ID:\s*({event_code}PBPS)"""
]
DupFields = [ "dest_user->account" ]
ParserVersion = "v1.0.0"
},

{
  Name = beyondtrust-privmgmt-kv-process-create-success-processstarttime
  Vendor = BeyondTrust
  Product = BeyondTrust
  TimeFormat = "yyyy-MM-dd HH:mm:ss.S"
  Conditions = [ """, ProcessStartTime="""", """, ProcessStartTimeMs="""" ]
  Fields = [
    """\WProcessStartTime="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+)""",
    """\WHostName ="({host}[^"]+)""",
    """\WEventNumber="({event_code}\d+)""",
    """\WUserName ="(({domain}[^\\"]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """\WEventDescription="({additional_info}[^"]+)""",
    """\WFileName ="({process_path}({process_dir}(?:(\w+:)?[^:"]+)?[\\\/])?({process_name}.+?))"""",
    """\WCommandLine="({process_command_line}.+?)",""",
    """\WProductName ="(<None>|({product_name}[^"]+))""",
    """\WPublisher="(<None>|({publisher}[^"]+))""",
    """\WReason="(<None>|({result_reason}[^"]+))""",
    """\WProcessGUID="({process_guid}[^"]+)""",
    """\WParentProcessUniqueID="({parent_process_guid}[^"]+)""",
    """\WPID="({process_id}[^"]+)""",
    """\WUserSID="({user_sid}[^"]+)""",
    """\WApplicationHash="({hash_md5}[^"]+)""",
    """\WActivityType="({operation_type}[^"]+)""",
  ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = "v1.0.0"
},

{
    Name = beyondtrust-privmgmt-kv-endpoint-login-success-userlogon
    Vendor = BeyondTrust
    Product = BeyondTrust
    TimeFormat = "MM/dd/yyyy HH:mm:ss a"
    Conditions = [ """SourceName =Avecto Defendpoint Service""", """Message=Detected user logon"""]
    Fields = [
      """ComputerName =({host}[^\s]+)""",
      """Message=({operation_type}.+?)\s+Command Line:""",
      """User Name:\s*(?:[A-F\d\-]{36}|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+User Domain SID:""",
      """User Domain Name:\s*({domain}[\w\.\-]{1,40}?)\s+User Domain Name""",
      """User SID:\s*({user_sid}.*?)\s+User Name""",
      """Administrator:\s*({admin}.*?)\s+Power User""",
      """Power User:\s*({power_user}.*?)\s+Workstyle""",
      """Workstyle:\s*({user_info}.*?)\s+Workstyle""",
      """IP4 Addresses:\s*[^,]+,({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(,|$|\s)""",
    ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = v1.0.0
},

{
    Name = beyondtrust-prividentity-kv-user-privilege-use-success-2038
    Vendor = BeyondTrust
    Product = BeyondTrust Privileged Identity
    TimeFormat = "yyyy-dd-MM'T'HH:mm:ss"
    Conditions = [ """sEventID="EVENT_ID_JOB_STARTING_ACCOUNT_ELEVATION_JOB"""", """<Event""", """sOriginatingApplicationName ="Privileged Identity"""" ]
    Fields = [
        """\d+:\d+:\d+\s+({host}[^\s]+)\s+<Event""",
        """dtPostTime="({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2})""",
        """dwAppSpecificEventID="({event_code}\d+)""",
        """sEventID="({event_name}[^"]+)""",
        """sOriginatingAccount="(({domain}[^"\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
        """sOriginatingSystem="({dest_host}[^"]+)""",
        """key="AccountToElevate"\s+value="(({account_domain}[^"\\]+)\\+)?({account}[^"]+)"""
    ]
    ParserVersion = "v1.0.0"
},

{
  Name = beyondtrust-powerbroker-kv-user-privilege-use-success-elevation
  Vendor = BeyondTrust
  Product = BeyondInsight
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [  """|BeyondTrust|""","""Application Requested Elevation""","""BeyondTrustBeyondInsightEventTypeID=28691""" ]
  Fields = [
    """\d\d:\d\d:\d\d ({host}[\w\-.]+) CEF""",
    """\|rt=({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)""",
    """BeyondTrustBeyondInsightUserName =(?: |({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+=)""",
    """BeyondTrustBeyondInsightPath=(?: |({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/"]+?))\s+\w+=)""",
    """BeyondTrustBeyondInsightAssetName =(?: |({src_host}.+?)\s+\w+=)""",
    """BeyondTrustBeyondInsightUserType=(?: |({privileges}.+?)\s*$)""",
    """deviceExternalId=({event_code}pbw|pbmac)""",
  ]
  ParserVersion = "v1.0.0"
},

{
Vendor = "BeyondTrust"
Product = "BeyondTrust Privileged Identity"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Fields = [
"""\d\d:\d\d:\d\d ({host}[\w\-.]+) CEF"""
"""rt=({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)"""
"""msg=({additional_info}.+?)\s+(\w+=|$)"""
"""dntdom=\[?({domain}.+?)\]?\s+(\w+=|$)"""
"""duser=(\\)*((?i)(user|admin|administrator)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+(\w+=|$)"""
"""cs3=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""CEF:\d+\|([^\|]+\|){3}({event_name}[^\|]+)\|"""
"""cs1=.+?({result}Success|Failure)"""
"""Impersonating user (({dest_domain}[^\\]+)(\\)+)?({dest_user}[^\s)]+)\)"""
]
Name = "beyondtrust-prividentity-cef-app-login-privilegedidentity"
Conditions = [
"""CEF:"""
"""|Privileged Identity|"""
"""|EVENT_ID_WEBAPP_LOGIN|"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = "BeyondTrust"
Product = "BeyondTrust Privileged Identity"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Fields = [
"""\d\d:\d\d:\d\d ({host}[\w\-.]+) CEF"""
"""rt=({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)"""
"""msg=({additional_info}.+?)\s+(\w+=|$)"""
"""dntdom=\[?({domain}.+?)\]?\s+(\w+=|$)"""
"""duser=(\\)*((?i)(user|admin|administrator)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+(\w+=|$)"""
"""cs3=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""CEF:\d+\|([^\|]+\|){3}({event_name}[^\|]+)\|"""
"""cs1=.+?({result}Success|Failure)"""
"""for '*\(({dest_host}[^)]+)\)'\[?({dest_domain}[^\\\]]+)\]?(\\)*({dest_user}[^'\s]+)'"""
]
Name = "beyondtrust-prividentity-cef-app-activity-success-idpassword"
Conditions = [
"""CEF:"""
"""|Privileged Identity|"""
"""|EVENT_ID_PASSWORD_"""
]
ParserVersion = "v1.0.0"
},


{
Vendor = "BeyondTrust"
Product = "BeyondTrust Privileged Identity"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Fields = [
  """CEF:([^\|]*\|){4}({operation}[^\|]+)"""
  """CEF:([^\|]*\|){5}({result}[^\|]+)"""
  """\Wrt=({time}\w+ \d+ \d\d\d\d \d+:\d+:\d+)"""
  """\Wshost=({host}[\w\-.]+)"""
  """\(running as user (({account_domain}[^\s\\]+)\\+)?({account}[^\s\\\)]+)\)"""
  """sntdom=({account_domain}[^\s]+)"""
  """suser=({account}[^\s]+)"""
  """\(user (({domain}[^\s\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\) \-\s+({additional_info}.+?)\s+(\w+=|$)"""
  """dntdom=({domain}[^\s]+)"""
  """duser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """group '({object}[^\']+)' on system """
  """dhost=({src_host}[\w\-.]+)"""
  """({app}Liebsoft)"""
]
Name = "beyondtrust-prividentity-cef-app-activity-elevationfailed"
Conditions = [
  """CEF:"""
  """|Liebsoft|"""
  """|EVENT_ID_JOB_ACCOUNT_ELEVATION_FAILED|"""
]
ParserVersion = "v1.0.0"
}

{
Vendor = "BeyondTrust"
Product = "BeyondTrust Privileged Identity"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Fields = [
  """CEF:([^\|]*\|){4}({operation}[^\|]+)"""
  """CEF:([^\|]*\|){5}({result}[^\|]+)"""
  """\Wrt=({time}\w+ \d+ \d\d\d\d \d+:\d+:\d+)"""
  """\Wshost=({host}[\w\-.]+)"""
  """\(running as user (({account_domain}[^\s\\]+)\\+)?({account}[^\s\\\)]+)\)"""
  """sntdom=({account_domain}[^\s]+)"""
  """suser=({account}[^\s]+)"""
  """\(user (({domain}[^\s\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\) \-\s+({additional_info}.+?)\s+(\w+=|$)"""
  """dntdom=({domain}[^\s]+)"""
  """duser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """group '({object}[^\']+)' on system """
  """dhost=({src_host}[\w\-.]+)"""
  """({app}Liebsoft)"""
]
Name = "beyondtrust-prividentity-cef-app-activity-jobaccount"
Conditions = [
  """CEF:"""
  """|Liebsoft|"""
  """|EVENT_ID_JOB_ACCOUNT_ELEVATED|"""
]
ParserVersion = "v1.0.0"
}

{
Vendor = "BeyondTrust"
Product = "BeyondTrust Privileged Identity"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Fields = [
  """CEF:([^\|]*\|){4}({operation}[^\|]+)"""
  """CEF:([^\|]*\|){5}({result}[^\|]+)"""
  """\Wrt=({time}\w+ \d+ \d\d\d\d \d+:\d+:\d+)"""
  """\Wshost=({host}[\w\-.]+)"""
  """\(running as user (({account_domain}[^\s\\]+)\\+)?({account}[^\s\\\)]+)\)"""
  """sntdom=({account_domain}[^\s]+)"""
  """suser=({account}[^\s]+)"""
  """\(user (({domain}[^\s\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\) \-\s+({additional_info}.+?)\s+(\w+=|$)"""
  """dntdom=({domain}[^\s]+)"""
  """duser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """group '({object}[^\']+)' on system """
  """dhost=({src_host}[\w\-.]+)"""
  """({app}Liebsoft)"""
]
Name = "beyondtrust-prividentity-cef-app-activity-accountdeelevated"
Conditions = [
  """CEF:"""
  """|Liebsoft|"""
  """|EVENT_ID_JOB_ACCOUNT_ELEVATION_DEELEVATED|"""
]
ParserVersion = "v1.0.0"
}

{
Vendor = "BeyondTrust"
Product = "BeyondTrust Privileged Identity"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Fields = [
  """CEF:([^\|]*\|){4}({operation}[^\|]+)"""
  """CEF:([^\|]*\|){5}({result}[^\|]+)"""
  """\Wrt=({time}\w+ \d+ \d\d\d\d \d+:\d+:\d+)"""
  """\Wshost=({host}[\w\-.]+)"""
  """\(running as user (({account_domain}[^\s\\]+)\\+)?({account}[^\s\\\)]+)\)"""
  """sntdom=({account_domain}[^\s]+)"""
  """suser=({account}[^\s]+)"""
  """\(user (({domain}[^\s\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\) \-\s+({additional_info}.+?)\s+(\w+=|$)"""
  """dntdom=({domain}[^\s]+)"""
  """duser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """group '({object}[^\']+)' on system """
  """dhost=({src_host}[\w\-.]+)"""
  """({app}Liebsoft)"""
]
Name = "beyondtrust-prividentity-cef-app-activity-deelevationfailed"
Conditions = [
  """CEF:"""
  """|Liebsoft|"""
  """|EVENT_ID_JOB_ACCOUNT_ELEVATION_DEELEVATION_FAILED|"""
]
ParserVersion = "v1.0.0"
}

{
Vendor = "BeyondTrust"
Product = "BeyondTrust Privileged Identity"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Fields = [
  """CEF:([^\|]*\|){4}({operation}[^\|]+)"""
  """CEF:([^\|]*\|){5}({result}[^\|]+)"""
  """\Wrt=({time}\w+ \d+ \d\d\d\d \d+:\d+:\d+)"""
  """\Wshost=({host}[\w\-.]+)"""
  """\(running as user (({account_domain}[^\s\\]+)\\+)?({account}[^\s\\\)]+)\)"""
  """sntdom=({account_domain}[^\s]+)"""
  """suser=({account}[^\s]+)"""
  """\(user (({domain}[^\s\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\) \-\s+({additional_info}.+?)\s+(\w+=|$)"""
  """dntdom=({domain}[^\s]+)"""
  """duser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """group '({object}[^\']+)' on system """
  """dhost=({src_host}[\w\-.]+)"""
  """({app}Liebsoft)"""
]
Name = "beyondtrust-prividentity-cef-app-activity-listaddedaccount"
Conditions = [
  """CEF:"""
  """|Liebsoft|"""
  """|EVENT_ID_SHARED_CREDENTIAL_LIST_ADDED_ACCOUNT|"""
]
ParserVersion = "v1.0.0"
}

{
  Name = beyondtrust-passwordsafe-json-app-login-success-beyondinsight
  Vendor = BeyondTrust
  Product = BeyondInsight
  TimeFormat = ["MM/dd/yyyy HH:mm:ss a","M/dd/yyyy HH:mm:ss a"]
  Conditions = [ """"vendor":"BeyondTrust"""", """"eventname":"Login"""", """"category":"PMM Login"""", """"product":"BeyondInsight"""", """"systemname":"PMM Login"""" ]
  Fields = [
    """"host":"({host}[^"]+)"""",
    """"createdate":"({time}\d{1,2}\/\d{1,2}\/\d\d\d\d\s\d{1,2}:\d{1,2}:\d{1,2}\s\w{1,2})"""",
    """"username":"(({domain}[^\"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """"(sourceip|ipaddress)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"sourcehost":"({src_host}[^"]+)"""",
    """"({app}BeyondInsight)"""",
    """"category":"({event_name}[^"]+)"""",
    """"eventname":"({additional_info}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"
},

{
  Name = beyondtrust-passwordsafe-json-app-login-success-applogin
  Vendor = BeyondTrust
  Product = BeyondInsight
  TimeFormat = ["MM/dd/yyyy HH:mm:ss a","M/dd/yyyy HH:mm:ss a"]
  Conditions = [ """"vendor":"BeyondTrust"""", """"eventname":"Login"""", """"category":"Login"""", """"product":"BeyondInsight"""", """"systemname":"Login"""" ]
  Fields = [
    """"host":"({host}[^"]+)"""",
    """"createdate":"({time}\d{1,2}\/\d{1,2}\/\d\d\d\d\s\d{1,2}:\d{1,2}:\d{1,2}\s\w{1,2})"""",
    """"username":"(({domain}[^\"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """"(sourceip|ipaddress)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"sourcehost":"({src_host}[^"]+)"""",
    """"({app}BeyondInsight)"""",
    """"category":"({event_name}[^"]+)"""",
    """"eventname":"({additional_info}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"
}

{
  Name = beyondtrust-passwordsafe-json-app-login-fail-loginfailure
  Vendor = BeyondTrust
  Product = BeyondInsight
  TimeFormat = ["MM/dd/yyyy HH:mm:ss a","M/dd/yyyy HH:mm:ss a"]
  Conditions = [ """"vendor":"BeyondTrust"""", """"eventname":"Login"""", """"category":"Login Failure"""", """"product":"BeyondInsight"""", """"message":"""", """"systemname":"Login Failure"""" ]
  Fields = [
    """"host":"({host}[^"]+)"""",
    """"createdate":"({time}\d{1,2}\/\d{1,2}\/\d\d\d\d\s\d{1,2}:\d{1,2}:\d{1,2}\s\w{1,2})"""",
    """"username":"(({domain}[^\"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """"(sourceip|ipaddress)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"sourcehost":"({src_host}[^"]+)"""",
    """"({app}BeyondInsight)"""",
    """"category":"({event_name}[^"]+)"""",
    """"eventname":"({additional_info}[^"]+)"""",
    """"message":"({failure_reason}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"
},

{
  Name = beyondtrust-b-kv-endpoint-login-success-loggedin
  Vendor = BeyondTrust
  Product = BeyondTrust
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """|Bomgar|Privileged Access|""", """sessionId=""", """dstUser=""" ]
  Fields = [
    """({app}Privileged Access)""",
    """\|Privileged Access\|([^\|]+\|){2}({operation}[^\|]+)\|""",
    """srcAddr=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """srcPort=({src_port}\d+)""",
    """srcHost=({src_host}[^\|]+)""",
    """\|dstUser=(({full_name}({first_name}[^\s\|]+)\s({last_name}[^\|]+))|({dest_user}[^\|]+))""",
    """\|srcUser=(\[Pinned\] )?(({full_name}({first_name}[^\s\|]+)\s({last_name}[^\|]+))|({email_address}[^\s@\|]+@[^\s@\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """msg=({additional_info}[^\|]+?)\s*\|""",
    """credentialName =({additional_info}[^\|]+)"""
  ]
  DupFields = [ "operation->event_name", "dest_user->object" ]
  ParserVersion = "v1.0.0"
},

${BeyondTrustParserTemplates.cef-beyondtrust-app-activity-events}{
  Name = beyondtrust-prividentity-cef-app-activity-success-pbpsadmin
  ParserVersion = v1.0.0
  Conditions = [ """cat=System""", """CEF:""", """|BeyondTrust|BeyondInsight|""", """|PBPS|Administrators|""" 
}
```