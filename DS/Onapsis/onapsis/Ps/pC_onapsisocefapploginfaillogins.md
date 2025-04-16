#### Parser Content
```Java
{
Name = "onapsis-o-cef-app-login-fail-logins"
Product = "Onapsis"
Conditions = [
"""CEF:"""
"""|Onapsis|OSP|"""
"""|All Failed Logins|"""
]
ParserVersion = "v1.0.0"

cef-edirectory-events.Fields} [
    """CEF:([^\|]*\|){5}({alert_name}[^\|]+)""",
    """CEF:([^\|]*\|){6}({alert_severity}[^\|]+)""",
    """sproc=({process_name}.*?)\s\w+=""", 
  ]
  DupFields = [ "alert_name->alert_type" ]
  ParserVersion = "v1.0.0"
},

{
Vendor = "Onapsis"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Fields = [
"""CEF:([^\|]*\|){5}\s*({event_name}[^\|]+?)\s*\|"""
"""\Wend=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)"""
"""\Wcat=(None|({category}.+?))(\s+\w+=|\s*$)"""
"""\Wdhost=(__EMPTY__|({dest_host}.+?))(\s+\w+=|\s*$)"""
"""\Wdpt=({dest_port}\d+)"""
"""\Wspt=({src_port}\d+)"""
"""\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Wproto=(None|({protocol}.+?))(\s+\w+=|\s*$)"""
"""\Wreason=(None|({failure_reason}.+?))(\s+\w+=|\s*$)"""
"""\WrequestClientApplication=(None|({app}.+?))(\s+\w+=|\s*$)"""
"""\Wshost=(None|({src_host}.+?))(\s+\w+=|\s*$)"""
"""\Wsuser=(None|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s*TAG:|\s+\w+=|\s*$)"""
"""\WTAG:\s*({tag}.+?)(\s*\w+=|\s*$)"""
]
Name = "onapsis-o-cef-app-login-success-onapsis"
Product = "Onapsis"
Conditions = [
"""CEF:"""
"""|Onapsis|OSP|"""
"""|All Successful Logins|"""
]
ParserVersion = "v1.0.0"
}

{
Vendor = "Onapsis"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Fields = [
"""CEF:([^\|]*\|){5}\s*({event_name}[^\|]+?)\s*\|"""
"""\Wend=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)"""
"""\Wcat=(None|({category}.+?))(\s+\w+=|\s*$)"""
"""\Wdhost=(__EMPTY__|({dest_host}.+?))(\s+\w+=|\s*$)"""
"""\Wdpt=({dest_port}\d+)"""
"""\Wspt=({src_port}\d+)"""
"""\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Wproto=(None|({protocol}.+?))(\s+\w+=|\s*$)"""
"""\Wreason=(None|({failure_reason}.+?))(\s+\w+=|\s*$)"""
"""\WrequestClientApplication=(None|({app}.+?))(\s+\w+=|\s*$)"""
"""\Wshost=(None|({src_host}.+?))(\s+\w+=|\s*$)"""
"""\Wsuser=(None|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s*TAG:|\s+\w+=|\s*$)"""
"""\WTAG:\s*({tag}.+?)(\s*\w+=|\s*$)"""
]
Name = "onapsis-o-cef-app-login-fail-logins"
Product = "Onapsis"
Conditions = [
"""CEF:"""
"""|Onapsis|OSP|"""
"""|All Failed Logins|"""
]
ParserVersion = "v1.0.0"
}

${MBMCParsersTemplates.cef-mbmc-security-alert} {
  Name = malwarebytes-ep-cef-alert-trigger-success-ipblock
  Conditions = [ """|Malwarebytes|MBMC|""", """|IPBLOCK|""" ]
  ParserVersion = "v1.0.0"
},

${OnapsisParsersTemplates.cef-onapsis-activity}{
  Name = onapsis-o-cef-alert-trigger-success-osp
  Product = Onapsis
  Conditions = [ """CEF:""", """|Onapsis|OSP|""", """OnapsisOSPPolicy=""" ]
  Fields = ${OnapsisParsersTemplates.cef-onapsis-activity.Fields}[
    """\Wcat=(None|({alert_type}.+?))(\s+\w+=|\s*$)""",
    """\Wsev=({alert_severity}\d+)""",
    """\Wmsg=(None|({alert_name}.+?))(\s+\w+=|\s*$)""",
  ]
  ParserVersion = "v1.0.0"
},

{
  Name = juniper-jn-cef-alert-trigger-success-cyphort
  Vendor = Juniper Networks
  Product = Juniper Advanced Threat Protection
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = ["""|Cyphort|Cortex|"""]
  Fields = [
    """lastActivityTime=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """\w+\s+\d+\s+\d\d:\d\d:\d\d\s+({host}[^\s]+)""",
    """\|Cyphort\|[^|]+?\|[^|]+?\|[^|]+?\|({alert_type}[^|]+?)\|""",
    """\|Cyphort\|[^|]+?\|[^|]+?\|[^|]+?\|({alert_name}[^|]+?)\|""",
    """\|Cyphort\|[^|]+?\|[^|]+?\|[^|]+?\|[^|]+?\|({alert_severity}[^|]+?)\|""",
    """\seventId=({alert_id}\d+)""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sfileName =({file_name}.+?)\s+\w+=""",
    """\surl=({url}[^\r\n]+)\s+""",
    """\smalwareSeverity=({alert_severity}.+?)\s+\w+=""",
    """\smalwareCategory=({alert_type}.+?)\s+\w+="""
  ]
  DupFields = ["file_name->process_name"]
  ParserVersion = "v1.0.0"
},

{
Name = "msdhcp-m-str-dhcp-session-success-dnsupdate"
Vendor = "MSDHCP"
Product = "MSDHCP"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
  """[][]"""
  """[DHCP]"""
  """ MSDHCP """
  """,DNS Update Successful,"""
]
Fields = [
  """\[\]\[\]\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\[({event_code}\d+)\]\[DHCP\]"""
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)\s+({host}[\w.\-]+)"""
  """"([^,]*,)\d+\/\d+\/\d+,\d+:\d+:\d+,({operation}[^,]+),(|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?),(|({dest_host}[\w\-.]+)),(|({dest_mac}[^,\s]+)),"""
]
DupFields = [
  "event_code->service_id"
]
ParserVersion = "v1.0.0"
},

{
Name = "nokia-vqip-kv-dhcp-session-success-dhcpsession"
Vendor = "Nokia VitalQIP"
Product = "Nokia VitalQIP"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """qip"""
  """DHCP_RenewLease"""
  """ Host="""
  """ Domain="""
]
Fields = [
  """: Host=({dest_host}[^\s]+)"""
  """ IP=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """Domain=({domain}[^\s]+)"""
]
DupFields = [
  "dest_host->user"
]
ParserVersion = "v1.0.0"
},

{
Name = "kemp-loadmaster-str-endpoint-login-success-loggedin"
Vendor = "Kemp"
Product = "Kemp LoadMaster"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """logger: User"""
  """ Logged in """
  """(Session: """
]
Fields = [
  """User\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\)"""
  """({event_name}Logged in)"""
  """({event_category}logger)"""
]
ParserVersion = "v1.0.0"
},

{
  Name = progress-pdatabase-str-endpoint-login-success-742
  Vendor = Progress
  Product = Progress Database
  TimeFormat = ["yyyy-MM-dd'@'HH:mm:ss.SSSZ","yyyy/MM/dd'@'HH:mm:ss.SSSZ"]
  Conditions = [ """ T-""", """ P-""", """(742)""", """ Login """ ]
  Fields = [
  """:\d\d:\d\d\s+({src_host}[^\s]+)\s+\[({time}\d\d\d\d\/\d\d\/\d\d@\d\d:\d\d:\d\d\.\d\d\d-\d\d\d\d)\]\s+({process_id}[^\s]+)\s+({thread_id}[^\s]+)\s+({severity}[^\s]+)\s+({service_name}TSRV)\s+\d:\s*\(({event_code}742)\)\s+({additional_info}({event_name}Login)[^,]+),\s+userid\s({user}[\w\.\-\!\#\^\~]{1,40}\$?)[^,]+,\son\s({dest_host}[^\s]+)\s[^"]+?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\.?\s+"?$"""
  ]
  ParserVersion = "v1.0.0"
},

{
  Name = extrahop-revealx-json-alert-trigger-success-sec
  Vendor = Extrahop
  Product = Extrahop Reveal(x)
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """categories""", """sec.""", """vendor":"ExtraHop""", """description""","""title"""]
  Fields = [
     """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+-\d+:\d+)\s*({host}[^\s]+)""",
     """"description":"({additional_info}[^"]+)""", 
     """"ipaddrs":\["({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?.+?offender""",
     """"ipaddrs":\["({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?.+?victim""",
     """"dnsNames":\["({src_host}[^."]+)(\.({domain}[^"]+))?".+?offender""",
     """"dnsNames":\["({dest_host}[^."]+)(\.({domain}[^"]+))?".+?victim""",
     """"title":"({alert_name}[^"]+)""",
     """"netbiosName":(null|"({sub_domain}[^"]+))""",
     """"dnsNames":\["({dns_query}[^"]+)"\]""",
     """"status":(null|"({status_msg}[^"\s]+))""",
     """"riskScore":(null|({original_risk_score}\d+))""",
  ]
  DupFields = ["alert_name->alert_type",
  "original_risk_score->alert_severity"]
  ParserVersion = "v1.0.0"
},

{
  Name = extrahop-revealx-json-alert-trigger-success-sec-1
  Vendor = Extrahop
  Product = Extrahop Reveal(x)
  TimeFormat = [ "MMM dd yyyy HH:mm:ss", "MMM dd yyyy HH:mm:ss Z" ]
  ExtractionType = json
  Conditions = [ """categories""", """sec.""", """"extrahop"""", """"event":""", """title"""]
  Fields = [
    """exa_json_path=$.event.start_time,exa_field_name=time""",
    """exa_json_path=$.event.detection_id,exa_field_name=alert_id""",
    """exa_json_path=$.event.title,exa_field_name=alert_name""",
    """exa_json_path=$.event.categories,exa_field_name=alert_type""",
    """exa_json_path=$.event.risk_score,exa_field_name=original_risk_score""",
    """exa_regex="object":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))
?",[^,]+?ipaddr""",
    """exa_json_path=$.event.participants[0].hostname,exa_regex=^({src_host}[\w\-.]+)$"""
    ]
      DupFields = [ "original_risk_score->alert_severity"]
    ParserVersion = "v1.0.0"
}

{
  Name = extrahop-revealx-json-alert-trigger-success-detection
  Vendor = Extrahop
  Product = Extrahop Reveal(x)
  TimeFormat = "yyyy/MM/dd HH:mm:ss.SSS"
  ExtractionType = json
  Conditions = [ """"detectionType"""", """"event":"Detection"""", """"title":"""", """"riskScore":"""]
  Fields = [
    """exa_json_path=$.startTime,exa_field_name=time""",
    """exa_json_path=$.id,exa_field_name=alert_id""",
    """exa_json_path=$.title,exa_field_name=alert_name""",
    """exa_json_path=$.event,exa_field_name=alert_type""",
    """exa_json_path=$.riskScore,exa_field_name=original_risk_score""",
    """exa_json_path=$.offenders,exa_regex=\["({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """exa_json_path=$.victims,exa_regex=\["({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",    
    """exa_json_path=$.description,exa_field_name=additional_info"""
  ]
        DupFields = [ "original_risk_score->alert_severity"]
  ParserVersion = "v1.0.0"
}

{
  Name = sophos-invincea-kv-alert-trigger-success-invincea
  Vendor = Sophos
  Product = Sophos Endpoint Protection
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """INVINCEA:""", """vendor=Invincea""", """product=Invincea""" ]
  Fields = [
        """\w{3}\s+\d{1,2}\s+\d{2}:\d{2}:\d{2}\s+({host}[^\s]+)""",
        """\s+name="({alert_name}[^\"]+)""",
        """severity=({alert_severity}\d+)\s+""",
        """src_host=({src_host}[^\s]+)""",
        """src_ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
        """product=({alert_type}[^\s]+)""",
        """request=({malware_url}.+?)\s+num_exec""",
        """src_user=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+src_host"""
  ]
  DupFields = ["host->dest_host", "malware_url->process_name"]
  ParserVersion = "v1.0.0"
},

{
  Name = mobileiron-mi-cef-alert-trigger-success-mobileiron
  Vendor = MobileIron
  Product = MobileIron
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Mobile Iron|""", """deviceSeverity=""", """dtz=""" ]
  Fields = [
    """ start=({time}\d{13}) """,
    """ eventId=({alert_id}\d+)""",
    """ cat=({alert_name}[^\s]+) """,
    """ suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+=""",
    """ act=({action}.+?)\s+\w+=""",
    """ dvc=({host}[\w\-.]+) """,
    """ agt=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))? """,
    """ act=({alert_name}.+?)\s+\w+=""",
    """ cat=({alert_type}.+?)\s+\w+=""",
    """ cs1=({additional_info}.+?)\s+\w+=""",
    """ cs3=\{({src_host}[\w\-.]+?)\}\s+\w+=""",
  ]
  ParserVersion = "v1.0.0"
},

{
  Name = kemp-loadmaster-str-alert-trigger-success-attempted
  Vendor = Kemp
  Product = Kemp LoadMaster
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ l7log:""", """ Attempted """, """ attack on """ ]
  Fields = [
    """\s({host}[\w\.\-]+)\s+\S+\s+\S+\s+l7log:""",
    """attack on\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\s+from\s+({malware_url}[^\(\s]+)\s+\(({additional_info}.+?)\)""",
    """\sAttempted\s+({alert_name}.+?)\s+on""",
  ]
  DupFields = [ alert_name->alert_type ]
  ParserVersion = "v1.0.0"
},

{
  Name = vectra-cd-json-alert-trigger-success-headendaddr
  Product = Vectra Cognito Detect
  Vendor = Vectra
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","MMM dd HH:mm:ss"]
  Conditions = [ """vectra_timestamp""","""headend_addr""","""category""","""threat"""]
  Fields =[
    """({time}\w+\s\d+\s\d+:\d+:\d+)""",
    """({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
    """"*d_type_vname"*:\s*"+({alert_name}[^"]+)""",
    """"*dvchost"*:\s*"+({host}[^"]+)""",
    """"*host_ip"*:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"*href"*:\s*"+({malware_url}[^"]+)""",
    """"*detection_id"*:\s+({alert_id}\d+)""",
    """"*dd_bytes_sent"*:\s+({bytes_out}\d+)""",
    """"*dd_dst_port"*:\s+({dest_port}\d+)""",
    """"*category"*:\s+"*({alert_type}[^"]+)""",
    """"*dd_bytes_rcvd"*:\s+({bytes_in}\d+)""",
    """"*dd_dst_dns"*:\s+"+({web_domain}[^"]+)"+,""",
    """"*severity"*:\s+({alert_severity}\d+)""",
    """"*host_name"*:\s+"+({src_host}[^"]+)""",
    """"*dd_dst_ip"*:\s+"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"*dd_proto"*:\s+"+({protocol}[^"]+)"+,""",
    """"*threat"*:\s+({threat_id}\d+)"""
  ]
  ParserVersion = "v1.0.0"
 },

{
Name = "logmein-ra-json-endpoint-login-success-raloginsuccess"
Vendor = "LogMeIn"
Product = "RemotelyAnywhere"
TimeFormat = "yyyy-MM-dd HH:mm:ss.S"
Conditions = [
  """"Windows_Remotely_Anywhere_Policy"""
  """ POLICY_NAME: """
  """RA_Login_Success"""
]
Fields = [
  """EVENT_DT:\s"+({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\.\d)""""
  """\sHOSTADDR:\s"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
  """\sHOSTNAME:\s+"+({host}[^"]+)"+\s"""
  """\sSession\s-\s({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\s-\sLogging in as '(({domain}\w+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)'."""
  """\sDESCRIPTION:\s"+({description}[^"]+)""""
  """\sRULE_NAME: "*({rule}[^"]+)""""
  """\sDOMAIN_NAME:\s+"+(unknown|null|({domain}[^"]+))"+\s"""
  """\sEVENT_TYPE_D:\s+"+({event_name}[^"]+)"+\s"""
  """\sEVENT_SEVERITY_D:\s+"+({alert_severity}[^"]+)"+\s"""
  """\sEVENT_PRIORITY:\s+"+({priority}[^"]+)"+\s"""
  """\sPOLICY_NAME:\s+"+({policy_name}[^"]+)"+\s"""
  """\sPROCESS_NAME:\s+"+(unknown|null|({process_path}[^"]+))"+\s"""
  """\sUSER_NAME:\s+"+(unknown|null|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"+\s"""
]
DupFields = [
  "event_name->event_category"
]
ParserVersion = "v1.0.0"
},

{
Vendor = "Symantec"
Product = "Symantec Critical System Protection"
TimeFormat = "yyyy-MM-dd HH:mm:ss.S"
Fields = [
"""\sHOSTNAME\s*:\s*"+({host}[^\s"]+)"""
"""\sEVENT_DT\s*:\s*"+({time}[^"]+)"""
"""\sUSER_NAME\s*:\s*"+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""\sRULE_NAME\s*:\s*"+({rule}[^"\s]+)"""
"""\sPOLICY_NAME\s*:\s*"+\s*({policy_name}[^"]+?)\s*"+?\s[^:]+:"""
"""\sPROCESS_PATH\s*:\s*"+({process_name}[^"\s]+)"""
"""SESSION_ID\s*:\s*"+({session_id}\d+)"""
"""Type of login\s*:\s*"*({login_type_text}[^"]+)"""
"""Parent Name\s*:\s*({parent_process_path}[^\s"]+)"""
"""\sEVENT_ID:\s*"+({event_code}\d+)"""
"""\sHOSTADDR:\s*"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sSVA_IP_ADDRESS:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sDOMAIN_NAME\s*:\s*"+\(?(none|({domain}[^"\s\)]+))"""
"""({result}(S|s)uccess)"""
"""({event_name}User Logged in)"""
]
DupFields = [
"host->dest_host"
]
Name = "symantec-csp-json-endpoint-login-success-userloggedin"
Conditions = [
"""SVA_IP_ADDRESS: """
""" USER_NAME:"""
"""User Logged in"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = "Symantec"
Product = "Symantec Critical System Protection"
TimeFormat = "yyyy-MM-dd HH:mm:ss.S"
Fields = [
"""\sHOSTNAME\s*:\s*"+({host}[^\s"]+)"""
"""\sEVENT_DT\s*:\s*"+({time}[^"]+)"""
"""\sUSER_NAME\s*:\s*"+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""\sRULE_NAME\s*:\s*"+({rule}[^"\s]+)"""
"""\sPOLICY_NAME\s*:\s*"+\s*({policy_name}[^"]+?)\s*"+?\s[^:]+:"""
"""\sPROCESS_PATH\s*:\s*"+({process_name}[^"\s]+)"""
"""SESSION_ID\s*:\s*"+({session_id}\d+)"""
"""Type of login\s*:\s*"*({login_type_text}[^"]+)"""
"""Parent Name\s*:\s*({parent_process_path}[^\s"]+)"""
"""\sEVENT_ID:\s*"+({event_code}\d+)"""
"""\sHOSTADDR:\s*"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sSVA_IP_ADDRESS:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sDOMAIN_NAME\s*:\s*"+({domain}[^"\s]+)"""
"""({result}(F|f)ailed)"""
"""({event_name}Failed Login)"""
]
DupFields = [
"host->dest_host"
]
Name = "symantec-csp-json-endpoint-login-fail-failedlogin"
Conditions = [
"""SVA_IP_ADDRESS: """
""" USER_NAME:"""
"""Failed Login"""
]
ParserVersion = "v1.0.0"
},

{
Name = "linux-ssh-json-ssh-traffic-success-sshlogon"
Vendor = "Unix"
Product = "Unix"
TimeFormat = "yyyy-MM-dd HH:mm:ss.S"
Conditions = [
  """SSH_Logon_"""
  """USER_TEXT: """
  """COLLECTORNAME: """
  """ ASSET_COLLECTORRID: """
  """SVA_IP_ADDRESS: """
]
Fields = [
  """EVENT_DT:\s\"+({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\.\d)\""""
  """\sHOSTADDR:\s\"+({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\""""
  """\sHOSTNAME:\s+\"+({host}[^\"]+)\"+\s"""
  """Remote From:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\sDESCRIPTION:\s\"+({description}[^\"]+)\""""
  """OSTYPE_D:\s\"+({os}[^\"]+)\"+\s"""
  """Session id:\s*({session_id}\d+)"""
  """Process Name:\s*(null|unknown|({process_name}\S+))"""
  """Parent Name:\s*(null|unknown|({parent_process_name}\S+))"""
  """Username:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """Port:\s*({src_port}\d+)"""
  """\sRULE_NAME: \"*({rule}[^\"]+)\""""
  """EVENT_TYPE_D:\s+\"+({event_name}[^\"]+)\"+\s"""
  """EVENT_ID:\s+\"+({login_id}[^\"]+)\"+\s"""
  """PROCESS_ID:\s+\"+(null|unknown|({process_id}[^\"]+))\"+\s"""
]
DupFields = [
  "event_name->event_category"
]
ParserVersion = "v1.0.0"
},

{
Name = "kemp-loadmaster-str-endpoint-login-success-loggedon"
Vendor = "Kemp"
Product = "Kemp LoadMaster"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """ l7log:"""
  """ logged on from """
]
Fields = [
  """\s({host}[\w\.\-]+)\s+\S+\s+\S+\s+l7log:"""
  """l7log:\s+(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[^\s:]+))"""
  """from\s+(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^\s:]+))"""
  """\sUser\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+logged"""
]
ParserVersion = "v1.0.0"
},

{
Name = "xsuite-x-kv-endpoint-login-success-connected"
Vendor = "xsuite"
Product = "xsuite"
TimeFormat = "yyyy-MM-dd HH:mm:ss z"
Conditions = [
  """xsuite["""
  """,connection,"""
  """ connected """
]
Fields = [
  """connected\sto\s({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})[:;]"""
  """connection,({dest_host}[\w.-]+),"""
  """({user_dn}CN\s*=\s*.+?)\",connection,"""
  """,\"?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\"?,connection,"""
]
ParserVersion = "v1.0.0"
},

{
Name = "extremenetworks-zwlanm-str-endpoint-login-fail-loginfailed"
Vendor = "Extreme Networks"
Product = "Zebra WLAN Management"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "MMM dd HH:mm:ss"]
Conditions = [
  """%"""
  """SYSTEM-3-LOGIN_FAIL:"""
  """Log-in failed"""
]
Fields = [
  """({time}\w+\s+\d+ \d+:\d+:\d+)"""
  """({time}\d{1,4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2})"""
  """\s+({host}[^\s]+)\s+({event_code}%\d*SYSTEM-3-LOGIN_FAIL):\s+Log-in ({result}failed) for user '({user}[\w\.\-\!\#\^\~]{1,40}\$?)'\s+from '({protocol}[^']+)\'"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"
},
${F5ParsersTemplates.f5-waf-activity-aa}{
  Name = f5-waf-kv-user-switch-success-sessionopened
  Conditions = [ """"log_type":"WAF"""", """"log_vendor":"f5"""", """session opened for user""", """(uid=""", """sshd:""", """_unix""" ]
  Fields = ${F5ParsersTemplates.f5-waf-activity-aa.Fields} [
    """\(uid=({user_uid}\d+)\)""",
    """session opened for user ({dest_user}[^\s]+) by""",
    """sshd\[({login_id}\d+)""",
    """({event_code}ssh)""",
  ]
  ParserVersion = "v1.0.0"
},

{
Name = "mariadb-m-str-database-activity-success-read"
Vendor = "MariaDB"
Product = "MariaDB"
TimeFormat = "yyyyMMdd HH:mm:ss"
Conditions = [
"""MariaDB:"""
""",READ,"""
]
Fields = [
"""MariaDB:\s({time}\d+\s\d\d:\d\d:\d\d)"""
"""\:\d{2}\,({host}[^\,]+)?\,({user}[\w\.\-\!\#\^\~]{1,40}\$?)?\,({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,({connection_id}\d+)?\,({query_id}\d+)?\,({db_operation}\w+)?\,({db_name}[^\,]+)?\,({object}[^\,]+)?"""
]
ParserVersion = "v1.0.0"
},

{
Name = "mariadb-m-str-database-activity-success-mariadb"
Vendor = "MariaDB"
Product = "MariaDB"
TimeFormat = "yyyyMMdd HH:mm:ss"
Conditions = [
""" mariadb """
""",READ,"""
]
Fields = [
""" mariadb ({time}\d{1,8} \d\d:\d\d:\d\d),"""
"""\:\d{2}\,(|({host}[^\,]+))\,(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\,(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?),(|({connection_id}\d+))\,(|({query_id}\d+))\,(|({db_operation}\w+))\,(|({db_name}[^\,]+))\,(|({object}[^\,]+)),"""
]
ParserVersion = "v1.0.0"
},

{
Name = "postgresql-p-cef-database-178272478"
Vendor = "PostgreSQL"
Product = "PostgreSQL"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""eventId="""
"""|PostgreSQL|PostgreSQL Audit|"""
]
Fields = [
"""\srt=({time}\d{13})\s*\w+="""
"""\scs2=(None|idle|idle\sin\stransaction|authentication|({db_query}.+?))\s*\w+="""
"""\scs3=(\[unknown\]|({db_user}.+?))\s*\w+="""
"""\scs4=((\[unknown\])|({db_name}.+?))\s*\w+="""
"""\scs6=\s*({additional_info}.+?)\s*\w+="""
"""\sshost=({src_host}[\w\-.]+?)\s*\w+="""
"""\sdvc=({host}[\w\-.]+)"""
"""\sdvchost=({host}[\w\-.]+)"""
"""CEF[^\|]+\|([^\|]*\|){4}({event_name}.+?)\s*\|"""
"""\sdtz=({dtz}.+?)\s*\w+="""
"""\sact=({action}.+?)\s*\w+="""
"""\seventId=({alert_id}.+?)\s*\w+="""
"""\ssuser=(N\/A|-|\[unknown\]|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*\w+="""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*\w+="""
]
ParserVersion = "v1.0.0"
},
{
Vendor = "Sybase"
Product = "Sybase"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Fields = [
""""database_name"+:"+({db_name}[^"]+?)""""
""""object_name"+:"+({db_object}[^"]+?)""""
""""event_desc"+:"+({db_query}({db_operation}\w+)[^"]+?)""""
""""extra_info"+:"+\s*({additional_info}[^"]+?)\s*""""
""""object_owner"+:"+({db_user}[^"]+?)""""
""""facets_environment"+:"+({host}[^"]+?)""""
""""event_time"+:"+({time}[^"]+?)""""
""""user_name"+:"+({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
]
Name = "sybase-s-json-database-activity-success-accesstodb"
Conditions = [
"""object_name"""
""""event_desc""""
""""access to database""""
""""database_name""""
""""extra_info""""
]
ParserVersion = "v1.0.0"
},

{
Vendor = "Sybase"
Product = "Sybase"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Fields = [
""""database_name"+:"+({db_name}[^"]+?)""""
""""object_name"+:"+({db_object}[^"]+?)""""
""""event_desc"+:"+({db_query}({db_operation}\w+)[^"]+?)""""
""""extra_info"+:"+\s*({additional_info}[^"]+?)\s*""""
""""object_owner"+:"+({db_user}[^"]+?)""""
""""facets_environment"+:"+({host}[^"]+?)""""
""""event_time"+:"+({time}[^"]+?)""""
""""user_name"+:"+({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
]
Name = "sybase-s-json-database-activity-success-eventdesc"
Conditions = [
"""object_name"""
""""event_desc""""
""""execution of stored procedure""""
""""database_name""""
""""extra_info""""
]
ParserVersion = "v1.0.0"
},
{
Vendor = "Apache"
Product = "Cassandra db"
TimeFormat = "epoch"
Fields = [
"""\|timestamp\:({time}\d{13})"""
"""\-\shost:\/({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\|source:\/({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\|operation:({additional_info}[^|]+?)\|\w+"""
"""\|authenticated:({db_user}[^\|]+)"""
"""\|type:({event_name}[^|]+)"""
]
DupFields = [
"db_user->user"
]
Name = "apache-cassandradb-str-database-activity-fail-auth"
Conditions = [
"""|category:AUTH|"""
"""|type:UNAUTHORIZED_ATTEMPT|"""
"""|authenticated:"""
"""|user:"""
"""|operation:"""
]
ParserVersion = "v1.0.0"
},
{
Name = "mariadb-m-str-database-delete-success-drop"
Vendor = "MariaDB"
Product = "MariaDB"
TimeFormat = "yyyyMMdd HH:mm:ss"
Conditions = [
"""MariaDB:"""
"""DROP"""
]
Fields = [
"""MariaDB:\s({time}\d+\s\d\d:\d\d:\d\d)"""
"""\:\d{2}\,({host}[^\,]+)?\,({user}[\w\.\-\!\#\^\~]{1,40}\$?)?\,({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,({connection_id}\d+)?\,({query_id}\d+)?\,({db_operation}\w+)?\,({db_name}[^\,]+)?\,({object}[^\,]+)?"""
]
ParserVersion = "v1.0.0"
},
{
Vendor = "Apache"
Product = "Cassandra db"
TimeFormat = "epoch"
Fields = [
"""\|timestamp\:({time}\d{13})"""
"""\-\shost:\/({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\|source:\/({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\|operation:({additional_info}[^|]+?)\s*$"""
"""\|authenticated:({db_user}[^\|]+)"""
"""\|type:({db_operation}[^|]+)"""
"""\|ks:({db_name}[^|]+)"""
"""\|operation:({additional_info}[^|\.]+)"""
]
DupFields = [
"additional_info->db_query"
]
Name = "apache-cassandradb-str-database-modify-success-ddl"
Conditions = [
"""|category:DDL|"""
"""|type:"""
"""|authenticated:"""
"""|user:"""
"""|operation:"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = "Nokia VitalQIP"
Product = "Nokia VitalQIP"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Fields = [
  """Host=({dest_host}[\w\-.]+)"""
  """IP=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """MAC=({dest_mac}\S+)"""
  """Domain=({domain}[^\s]+)"""
]
Name = "nokia-vqip-kv-dhcp-session-success-lucentdhcpservice"
Conditions = [
  """ Lucent_DHCP_Service"""
  """]: DHCP_GrantLease: """
]
ParserVersion = "v1.0.0"
},

{
Name = "mariadb-m-kv-database-modify-success-alter"
Vendor = "MariaDB"
Product = "MariaDB"
TimeFormat = "yyyyMMdd HH:mm:ss"
Conditions = [
"""MariaDB:"""
"""ALTER"""
]
Fields = [
"""MariaDB:\s({time}\d+\s\d\d:\d\d:\d\d)"""
"""\:\d{2}\,({host}[^\,]+)?\,({user}[\w\.\-\!\#\^\~]{1,40}\$?)?\,({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,({connection_id}\d+)?\,({query_id}\d+)?\,({db_operation}\w+)?\,({db_name}[^\,]+)?\,({object}[^\,]+)?"""
]
ParserVersion = "v1.0.0"
},

{
Name = "mariadb-m-kv-database-modify-success-create"
Vendor = "MariaDB"
Product = "MariaDB"
TimeFormat = "yyyyMMdd HH:mm:ss"
Conditions = [
"""MariaDB:"""
"""CREATE"""
]
Fields = [
"""MariaDB:\s({time}\d+\s\d\d:\d\d:\d\d)"""
"""\:\d{2}\,({host}[^\,]+)?\,({user}[\w\.\-\!\#\^\~]{1,40}\$?)?\,({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,({connection_id}\d+)?\,({query_id}\d+)?\,({db_operation}\w+)?\,({db_name}[^\,]+)?\,({object}[^\,]+)?"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = "Nokia VitalQIP"
Product = "Nokia VitalQIP"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Fields = [
  """Host=({dest_host}[\w\-.]+)"""
  """IP=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """MAC=({dest_mac}\S+)"""
  """Domain=({domain}[^\s]+)"""
]
Name = "nokia-vqip-kv-dhcp-session-success-lucentdhcpservice-1"
Conditions = [
  """ Lucent_DHCP_Service"""
  """]: DHCP_RenewLease: """
]
ParserVersion = "v1.0.0"
},

{
Name = "mariadb-m-str-database-modify-success-write"
Vendor = "MariaDB"
Product = "MariaDB"
TimeFormat = "yyyyMMdd HH:mm:ss"
Conditions = [
""" mariadb """
""",WRITE,"""
]
Fields = [
""" mariadb ({time}\d{1,8} \d\d:\d\d:\d\d),"""
"""\:\d{2}\,(|({host}[^\,]+))\,(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\,(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?),(|({connection_id}\d+))\,(|({query_id}\d+))\,(|({db_operation}\w+))\,(|({db_name}[^\,]+))\,(|({object}[^\,]+)),"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = "MasterSAM"
Product = "MasterSAM PAM"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
Fields = [
  """({host}[\w\-.]+)\s+Event Time:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+)"""
  """\WUser:\s*(({domain}[^\\\s]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """\Wname=({dest_host}[\w\-.]+)\s+(\w+=|$)"""
  """\Whost=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\Wprotocol=({protocol}.+?)\s+(\w+=|$)"""
  """\Wstatus=({result}.+?)\s+(\w+=|$)"""
  """\Wfailed_message=({failure_reason}.+?)\s+(\w+=|$)"""
  """\WActivity:\s*({operation}.+?)\s+User:"""
]
Name = "mastersam-pam-kv-endpoint-login-success-connect"
Conditions = [
  """ Activity:connect """
]
ParserVersion = "v1.0.0"
},

${MongoDBParserTemplates.mongodb-database-events}{
  Name = "mongodb-m-json-database-modify-success-createcollection"
  Conditions = [ """"atype" :""", """"createCollection"""", """"ts"""", """"local" : {""", """"param" :""", """"users" : [""" ]
  ParserVersion = "v1.0.0"
},

${MongoDBParserTemplates.mongodb-database-events}{
  Name = "mongodb-m-json-database-modify-success-createdb"
  Conditions = [ """"atype" :""", """"createDatabase"""", """"ts"""", """"local" : {""", """"param" :""", """"users" : [""" ]
  ParserVersion = "v1.0.0"
},


{
Name = "mysql-m-json-database-query-success-activity"
Vendor = "Mysql"
Product = "Mysql"
TimeFormat = "epoch"
ExtractionType = json
Conditions = [
""""msg-type":"activity""""
""""query":"""
]
Fields = [
  """"date":"({time}\d{13})""""
  """"user":"({db_user}[^"]+)""""
  """"ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
  """"host":"({dest_host}[^"]+)""""
  """"_os":"({os}[^"]+)""""
  """"_client_name":"({app}[^"]+)""""
  """"rows":"({response_size}\d+)""""
  """"pid":"({process_id}[^"]+)""""
  """"os_user":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
  """"status":"({action}[^"]+)""""
  """"cmd":"({db_operation}[^"]+)""""
  """"db":"({db_name}[^"]+)""""
  """"name":"({db_object}[^"]+)""""
  """"query":"({db_query}[^"]+)""""
  """exa_json_path=$.date,exa_field_name=time""",
  """exa_json_path=$.user,exa_field_name=db_user""",
  """exa_json_path=$.ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """exa_json_path=$.host,exa_field_name=dest_host""",
  """exa_json_path=$.connect_attrs._os,exa_field_name=os""",
  """exa_json_path=$.connect_attrs._client_name,exa_field_name=app""",
  """exa_json_path=$.rows,exa_field_name=response_size""",
  """exa_json_path=$.pid,exa_field_name=process_id""",
  """exa_json_path=$.os_user,exa_field_name=user""",
  """exa_json_path=$.status,exa_field_name=action""",
  """exa_json_path=$.cmd,exa_field_name=db_operation""",
  """exa_json_path=$.objects[0].db,exa_field_name=db_name""",
  """exa_json_path=$.objects[0].name,exa_field_name=db_object""",
  """exa_json_path=$.query,exa_field_name=db_query""",
]
DupFields = [
"dest_host->host"
]
ParserVersion = "v1.0.0"
},

{
Name = "onapsis-o-kv-database-modify-success-dbactivity"
Vendor = "Onapsis"
Product = "Onapsis"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""", db_table="""
""", action="""
""", user_name="""
""", user_id="""
]
Fields = [
"""<.*?>\w+ \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} ({host}[\w\.-]+?) ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
""", user_name=\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*,"""
""", user_id=\s*({user_id}[^,]+?)\s*,"""
""", action=\s*({db_operation}[^,]+?)\s*,"""
""", db_table\s*=({table_name}[^,]+?)\s*,"""
""", ({additional_info}change\..+change\..+?="+.+?"+)"""
""", request_id=\s*({alert_id}[^,]+?)\s*,"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"
},

${GoAnywhereParsersTemplates.goanywhere-events-2}{
  Name = goanywhere-gamft-kv-endpoint-login-success-loginsuccessful-1
  Conditions = [ """GoACHevent_type="Login Successful"""", """GoACHcommand="Login"""", """GoACHremote_ip="""", """GoACHuser_name="""" ]
  ParserVersion = v1.0.0
},

{
Vendor = "Portnox"
Product = "Portnox CLEAR"
TimeFormat = "epoch"
Fields = [
"""start=({time}\d{13})"""
"""CEF:([^|]*\|){4}({event_code}\d+)"""
"""CEF:([^|]*\|){5}({event_name}[^|]+)"""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""cs4=(unknown|({auth_method}[^=]+?))\s\w+="""
"""cs2=({policy_name}[^=]+?)\s\w+="""
"""msg=({additional_info}[^=]+?)\s\w+="""
"""duser=(({domain}[^\\=]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
]
Name = "portox-clear-cef-endpoint-login-fail-accessdenied"
Conditions = [
"""|Portnox"""
"""|CLEAR|"""
"""act=System"""
"""Access denied"""
]
ParserVersion = "v1.0.0"
}

{
Vendor = "Portnox"
Product = "Portnox CLEAR"
TimeFormat = "epoch"
Fields = [
"""start=({time}\d{13})"""
"""CEF:([^|]*\|){4}({event_code}\d+)"""
"""CEF:([^|]*\|){5}({event_name}[^|]+)"""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""cs4=(unknown|({auth_method}[^=]+?))\s\w+="""
"""cs2=({policy_name}[^=]+?)\s\w+="""
"""msg=({additional_info}[^=]+?)\s\w+="""
]
Name = "portox-clear-cef-endpoint-login-fail-authreject"
Conditions = [
"""|Portnox"""
"""|CLEAR|"""
"""act=Access"""
"""RADIUS failed to authenticate"""
"""'Authentication rejected'"""
]
ParserVersion = "v1.0.0"
}

{
Vendor = "Portnox"
Product = "Portnox CLEAR"
TimeFormat = "epoch"
Fields = [
"""start=({time}\d{13})"""
"""CEF:([^|]*\|){4}({event_code}\d+)"""
"""CEF:([^|]*\|){5}({event_name}[^|]+)"""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""cs4=(unknown|({auth_method}[^=]+?))\s\w+="""
"""cs2=({policy_name}[^=]+?)\s\w+="""
"""msg=({additional_info}[^=]+?)\s\w+="""
"""duser=(({domain}[^\\=]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
]
Name = "portox-clear-cef-endpoint-login-fail-accountnotfound"
Conditions = [
"""|Portnox"""
"""|CLEAR|"""
"""act=Access"""
"""account is not found"""
"""access was denied"""
]
ParserVersion = "v1.0.0"
}

{
Vendor = "Portnox"
Product = "Portnox CLEAR"
TimeFormat = "epoch"
Fields = [
"""start=({time}\d{13})"""
"""CEF:([^|]*\|){4}({event_code}\d+)"""
"""CEF:([^|]*\|){5}({event_name}[^|]+)"""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""cs4=(unknown|({auth_method}[^=]+?))\s\w+="""
"""cs2=({policy_name}[^=]+?)\s\w+="""
"""msg=({additional_info}[^=]+?)\s\w+="""
"""duser=(({domain}[^\\=]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
]
Name = "portox-clear-cef-endpoint-login-fail-macbypassdenied"
Conditions = [
"""|Portnox"""
"""|CLEAR|"""
"""act=Access"""
"""|MAC bypass denied|"""
]
ParserVersion = "v1.0.0"
}

{
Vendor = "Portnox"
Product = "Portnox CLEAR"
TimeFormat = "epoch"
Fields = [
"""start=({time}\d{13})"""
"""CEF:([^|]*\|){4}({event_code}\d+)"""
"""CEF:([^|]*\|){5}({event_name}[^|]+)"""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""cs4=(unknown|({auth_method}[^=]+?))\s\w+="""
"""cs2=({policy_name}[^=]+?)\s\w+="""
"""msg=({additional_info}[^=]+?)\s\w+="""
"""duser=(({domain}[^\\=]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
]
Name = "portox-clear-cef-endpoint-login-success-deviceauthsuccess"
Conditions = [
"""|Portnox"""
"""|CLEAR|"""
"""authentication success"""
"""act=Access """
"""The device was successfully authenticated"""
]
ParserVersion = "v1.0.0"
}

{
Vendor = "Portnox"
Product = "Portnox CLEAR"
TimeFormat = "epoch"
Fields = [
"""start=({time}\d{13})"""
"""CEF:([^|]*\|){4}({event_code}\d+)"""
"""CEF:([^|]*\|){5}({event_name}[^|]+)"""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""cs4=(unknown|({auth_method}[^=]+?))\s\w+="""
"""cs2=({policy_name}[^=]+?)\s\w+="""
"""msg=({additional_info}[^=]+?)\s\w+="""
]
Name = "portox-clear-cef-endpoint-login-success-guestauthsuccess"
Conditions = [
"""|Portnox"""
"""|CLEAR|"""
"""|Guest authentication success|"""
"""act=Access """
"""successfully authenticated"""
]
ParserVersion = "v1.0.0"
},

${MasterSAMParsersTemplates.mastersam-pam-events}{
  Name = mastersam-pam-kv-endpoint-authentication-fail-loginfail
  Conditions = [ """ Activity:login_fail """ ]
  ParserVersion = "v1.0.0"
},

${MasterSAMParsersTemplates.mastersam-pam-events}{
  Name = mastersam-pam-kv-endpoint-authentication-fail-otpfailed
  Conditions = [ """ Activity:login_verified_otp_failed """ ]
  ParserVersion = "v1.0.0"
},

${MasterSAMParsersTemplates.mastersam-pam-events}{
  Name = mastersam-pam-kv-endpoint-authentication-success-login
  Conditions = [ """ Activity:login """ ]
  ParserVersion = "v1.0.0"
},

${MasterSAMParsersTemplates.mastersam-pam-events}{
  Name = mastersam-pam-kv-endpoint-authentication-success-verifiedotp
  Conditions = [ """ Activity:login_verified_otp """ ]
  ParserVersion = "v1.0.0"
}

{
Vendor = "Apache"
Product = "Cassandra db"
TimeFormat = "epoch"
Fields = [
  """\|timestamp\:({time}\d{13})"""
  """\-\shost:\/({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\|source:\/({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\|operation:({additional_info}[^|]+?)\s*$"""
  """\|authenticated:({db_user}[^\|]+)"""
  """\|type:({event_name}[^|]+)"""
]
DupFields = [
  "db_user->user"
]
Name = apache-cassandradb-kv-database-login-success-auth
Conditions = [
  """|category:AUTH|"""
  """|type:LOGIN|"""
  """|authenticated:"""
  """|user:"""
  """|operation:"""
]
ParserVersion = "v1.0.0"
},

{
Name = sybase-s-cef-database-login-success-login
Vendor = "Sybase"
Product = "Sybase"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|Sybase|ASE Audit|"""
  """msg=Log in"""
]
Fields = [
  """\Wrt=({time}\d{13})"""
  """\Wdvc=({host}[A-Fa-f:\d.]+)"""
  """\Wdvchost=({host}[\w\-.]+)"""
  """\Wshost=({src_host}[\w\-.]+)"""
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wsuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """\Wdhost=({dest_host}[\w\-.]+)"""
  """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\Wcs6=({db_name}.+?)\s+\w+=.+?cs6Label=Database Name"""
  """\Wcs6Label=Database Name.+?cs6=({db_name}.+?)\s+\w+="""
  """\Wcs4=({result}.+?)\s+\w+=.+?cs4Label=Result"""
  """\Wcs4Label=Result.+?cs4=({result}.+?)\s+\w+="""
  """({app}Sybase)"""
]
DupFields = [
  "user->user"
]
ParserVersion = "v1.0.0"
},

{
Name = sybase-s-json-database-login-success-login
Vendor = "Sybase"
Product = "Sybase"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """object_name"""
  """"event_desc""""
  """"login""""
  """"database_name""""
  """"extra_info""""
]
Fields = [
  """"database_name"+:"+({db_name}[^"]+?)""""
  """"object_name"+:"+({db_object}[^"]+?)""""
  """"event_desc"+:"+({event_name}[^"]+?)""""
  """"extra_info"+:"+\s*({additional_info}[^"]+?)\s*""""
  """"object_owner"+:"+({db_user}[^"]+?)""""
  """"facets_environment"+:"+({host}[^"]+?)""""
  """"event_time"+:"+({time}[^"]+?)""""
  """"user_name"+:"+({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
]
ParserVersion = "v1.0.0"
},

{
Name = jsonar-sonarg-json-database-login-success-sonarw
Vendor = "jSONAR"
Product = "SonarG"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """ sonarw """
  """"$date":"""
  """"OS User":"""
  """"Database Name":"""
]
Fields = [
  """({host}[\w.\-]+) sonarw """
  """"\$date":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
  """"DB User Name":"(({db_domain}[^\\"]+)\\+)?(SYSTEM|({db_user}[^\\"]+))"""
  """"OS User":"(({domain}[^\\"]+)\\+)?(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """"Server IP":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """"Service Name":"({service_name}[^"]+)"""
  """"Server Host Name":"({dest_host}[\w\-.]+)"""
  """"Client Host Name":"({src_host}[\w\-.]+)"""
  """"Database Name":"({db_name}[^"]+)"""
  """Client IP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"
},

{
  Name = jsonar-sonarg-leef-database-login-success-logout
  Vendor = jSONAR
  Product = SonarG
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """ sonarw """, """|jSonar|sonarw|""", """LEEF:""", """DB User Name =""", """Session Activity Type=""" ]
  Fields = [
    """({host}[\w.\-]+) sonarw """,
    """Start=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """DB User Name =(({email_address}[^@\s]+@[^\s]+?)|(({db_domain}[^\\=]+?)\\)?({db_user}[^=]+?))\s+OS""",
    """Server IP=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """Server Host Name =({service_name}[^\s]+)""",
    """Client IP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """OS User=(null|((({domain}[^\\=]+?)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+Server""",
    """Session Activity Type=({event_name}[^=]+?)\s+Server IP="""
  ]
  ParserVersion = "v1.0.0"
  DupFields = [ "email_address->db_user" 
}
```