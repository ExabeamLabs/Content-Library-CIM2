#### Parser Content
```Java
{
Name = "forcepoint-wsg-cef-http-session-success-httpurllogged"
Conditions = [
"""CEF:"""
"""|FORCEPOINT|"""
"""|HTTP_URL-Logged|"""
]
ParserVersion = "v1.0.0"

cef-onapsis-activity.Fields}[
    """\Wcat=(None|({alert_type}.+?))(\s+\w+=|\s*$)""",
    """\Wsev=({alert_severity}\d+)""",
    """\Wmsg=(None|({alert_name}.+?))(\s+\w+=|\s*$)""",
  ]
  ParserVersion = "v1.0.0"
},

{
Vendor = "Auth0"
Product = "Auth0"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Fields = [
"""exa_json_path=$..date,exa_field_name=time"""
"""exa_json_path=$..hostname,exa_field_name=host"""
"""exa_json_path=$..description,exa_field_name=additional_info"""
"""exa_json_path=$..ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""exa_json_path=$..user_name,exa_regex=(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^,]+))?)"""
"""exa_json_path=$..user_id,exa_regex=((({auth_type}[^|"]+)\|({domain}[^|"]+)\|({user}[\w\.\-\!\#\^\~]{1,40}\$?))|(({=auth_type}[^|"]+)\|))"""
"""exa_json_path=$..client_name,exa_field_name=app"""
"""exa_json_path=$..user_agent,exa_field_name=user_agent"""
"""exa_json_path=$..severity,exa_field_name=alert_severity"""
"""exa_regex=({alert_name}pwd_leak)"""
]
Name = "auth0-a-json-alert-trigger-success-pwdleak"
Conditions = [
""""type":"pwd_leak""""
""""user_id""""
""""client_id""""
]
ExtractionType = json
ParserVersion = "v1.0.0"
},

{
Vendor = "Forcepoint"
Product = "Websense Security Gateway"
TimeFormat = "epoch"
Fields = [
"""CEF:\s+\d+\|([^\|]+\|){4}({operation}[^\|]+)"""
"""ahost=\s*({host}.+?)(\s\w+=)"""
"""\Wrt=({time}\d{13})"""
"""src=\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))."""
"""dhost=\s*({dest_host}.+?)(\s\w+=)"""
"""dst=\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))(\s\w+=)"""
"""amac=\s*({src_mac}.+?)(\s\w+=)"""
"""dvc=\s*({src_host}.+?)(\s\w+=)"""
"""app=\s*({protocol}.+?)(\s\w+=)"""
"""\Win=({bytes_in}\d+)"""
"""\Wout=({bytes_out}\d+)"""
"""\Wspt=({src_port}\d+)"""
"""\Wdpt=({dest_port}\d+)"""
"""\sdeviceInboundInterface=({src_interface}.+?)\s*\w+="""
"""\sdeviceOutboundInterface=({dest_interface}.+?)\s*\w+="""
"""\sproto=({protocol}.+?)\s*\w+="""
"""\Wmsg=(-|({url}(({protocol}[^:\\\/\s,"]+):[\\\/]+)?(({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})|({web_domain}[^\\\/\s:,"]+))?(:({dest_port}\d+))?({uri_path}\/[^\s\?"]*)?({uri_query}\?[^"\s]*)?))"""
]
Name = "forcepoint-wsg-cef-http-session-success-httpurllogged"
Conditions = [
"""CEF:"""
"""|FORCEPOINT|"""
"""|HTTP_URL-Logged|"""
]
ParserVersion = "v1.0.0"
},

{
Name = "sangfor-ngaf-kv-http-session-websitebrowsing"
Vendor = "Sangfor"
Product = "Sangfor NGAF"
TimeFormat = "yyyy-MM-dd HH:mm:ssZ"
Conditions = [
"""type: website browsing"""
"""<Identifier>ZC01_NTTDHK-FWL-002</Identifier>"""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d[\+\-]\d+:\d+)\s+\S+\s+fwlog:"""
"""<Identifier>ZC01_({host}[\w\-.]+)<\/Identifier>"""
"""user:\s*\((null|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)"""
"""policy name:\s*({policy_name}[^,"]+)"""
"""Src IP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""Dst IP:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""application:\s*({categories}({category}[^;,"]+)[^,]*)"""
"""action:\s*({action}[^,"]+)"""
"""URL:\s*(-|({url}(({protocol}[^:\\\/\s,"]+):[\\\/]+)?({web_domain}[^\\\/\s:,"]+)(:({dest_port}\d+))?({uri_path}\/[^\s\?",]*)?({uri_query}\?[^"\s]*)?))""""
]
ParserVersion = "v1.0.0"
},

{
Name = "squid-s-csv-http-session-evt"
Vendor = "Squid"
Product = "Squid"
TimeFormat = "yyyy-MM-dd HH:mm:ssZ"
Conditions = [
"""[EVT_"""
""",tk_url="""
""",tk_protocol="""
]
Fields = [
"""\Wtk_date_field=({time}[^,"]+)"""
"""\Wtk_server_ip=({host}[A-Fa-f:\d.]+)"""
"""\Wtk_server=({host}[\w\-.]+)"""
"""\Wtk_username=(({full_name}\w+(\s+\w+)+)|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),"""
"""\Wtk_client_ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wtk_url=(-|({url}(({protocol}[^:\\\/\s,]+):[\\\/]+)?(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({web_domain}[a-zA-z0-9.\-_]+(\.[a-zA-Z]{2,})?))(:\d+)?({uri_path}\/[^\s\?",]*)?({uri_query}\?[^"\s,]*)?))"""
"""\Wtk_protocol=({protocol}[^,"]+)"""
"""\Wtk_category=(0|({categories}({category}[^,";\/]+)[^,]*))"""
"""\Wtk_file_name=({uri_path}[^,"]+)"""
"""\Wtk_operation=({method}[^,"]+)"""
"""\Wtk_mime_content=(none|({mime}[^,"]+))"""
"""\Wtk_scan_type=({scan_type}[^,"]+)"""
"""\Wtk_rule_name=({rule}[^,"]+)"""
"""\Wtk_filter_action=({action}[^,"\s]+)"""
"""\[({result}EVT_\w+)\s*\|"""
]
ParserVersion = "v1.0.0"
},

{
  Name = forcepoint-ngfw-cef-network-session-fail-fwconnectiondiscarded
  Vendor = Forcepoint
  Product = Forcepoint Next-Gen Firewall
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """CEF:""", """|FORCEPOINT|Firewall|""", """|1001|FW_Connection-Discarded|""" ]
  Fields=[
    """\Wrt=({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
    """dvchost=({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """act=({action}[^=]+)\s\w+=""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """spt=({src_port}\d+)""",
    """dpt=({dest_port}\d+)""",
    """proto=({protocol}[^=]+?)\s\w+=""",
    """CEF:([^|]*\|){4}({event_code}[^|]+?)\|({event_name}[^|]+)\|""",
    """msg=({additional_info}[^"]+?)\s+\w+=""",
    """\Wout=({bytes_out}\d+)""",
    """\Win=({bytes_in}\d+)""",
    """deviceInboundInterface=({src_interface}[^=]+)\s\w+=""",
    """deviceOutboundInterface=({dest_interface}[^=]+)\s\w+="""
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
  """:\d\d:\d\d\s+({src_host}[^\s]+)\s+\[({time}\d\d\d\d\/\d\d\/\d\d@\d\d:\d\d:\d\d\.\d\d\d-\d\d\d\d)\]\s+({process_id}[^\s]+)\s+({thread_id}[^\s]+)\s+({severity}[^\s]+)\s+({service_name}TSRV)\s+\d:\s*\(({event_code}742)\)\s+({additional_info}({event_name}Login)[^,]+),\s+userid\s({user}[\w\.\-\!\#\^\~]{1,40}\$?)[^,]+,\son\s({dest_host}[^\s]+)\s[^"]+?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\.?\s+"?$"""
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
     """"ipaddrs":\["({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?.+?offender""",
     """"ipaddrs":\["({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?.+?victim""",
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
    """exa_json_path=$.offenders,exa_regex=\["({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """exa_json_path=$.victims,exa_regex=\["({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",    
    """exa_json_path=$.description,exa_field_name=additional_info"""
  ]
        DupFields = [ "original_risk_score->alert_severity"]
  ParserVersion = "v1.0.0"
}

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
    """"*host_ip"*:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"*href"*:\s*"+({url}[^"]+)""",
    """"*detection_id"*:\s+({alert_id}\d+)""",
    """"*dd_bytes_sent"*:\s+({bytes_out}\d+)""",
    """"*dd_dst_port"*:\s+({dest_port}\d+)""",
    """"*category"*:\s+"*({alert_type}[^"]+)""",
    """"*dd_bytes_rcvd"*:\s+({bytes_in}\d+)""",
    """"*dd_dst_dns"*:\s+"+({web_domain}[^"]+)"+,""",
    """"*severity"*:\s+({alert_severity}\d+)""",
    """"*host_name"*:\s+"+({src_host}[^"]+)""",
    """"*dd_dst_ip"*:\s+"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"*dd_proto"*:\s+"+({protocol}[^"]+)"+,""",
    """"*threat"*:\s+({user_threat_level}\d+)"""
    """"*certainty"*:\s+({user_threat_certainty}\d+)"""
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
"""\:\d{2}\,({host}[^\,]+)?\,({user}[\w\.\-\!\#\^\~]{1,40}\$?)?\,({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,({connection_id}\d+)?\,({query_id}\d+)?\,({db_operation}\w+)?\,({db_name}[^\,]+)?\,({object}[^\,]+)?"""
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
"""\:\d{2}\,(|({host}[^\,]+))\,(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\,(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?),(|({connection_id}\d+))\,(|({query_id}\d+))\,(|({db_operation}\w+))\,(|({db_name}[^\,]+))\,(|({object}[^\,]+)),"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = "Apache"
Product = "Cassandra db"
TimeFormat = "epoch"
Fields = [
"""\|timestamp\:({time}\d{13})"""
"""\-\shost:\/({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\|source:\/({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
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
"""\:\d{2}\,({host}[^\,]+)?\,({user}[\w\.\-\!\#\^\~]{1,40}\$?)?\,({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,({connection_id}\d+)?\,({query_id}\d+)?\,({db_operation}\w+)?\,({db_name}[^\,]+)?\,({object}[^\,]+)?"""
]
ParserVersion = "v1.0.0"
},
{
Vendor = "Apache"
Product = "Cassandra db"
TimeFormat = "epoch"
Fields = [
"""\|timestamp\:({time}\d{13})"""
"""\-\shost:\/({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\|source:\/({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
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
"""\:\d{2}\,({host}[^\,]+)?\,({user}[\w\.\-\!\#\^\~]{1,40}\$?)?\,({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,({connection_id}\d+)?\,({query_id}\d+)?\,({db_operation}\w+)?\,({db_name}[^\,]+)?\,({object}[^\,]+)?"""
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
"""\:\d{2}\,({host}[^\,]+)?\,({user}[\w\.\-\!\#\^\~]{1,40}\$?)?\,({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,({connection_id}\d+)?\,({query_id}\d+)?\,({db_operation}\w+)?\,({db_name}[^\,]+)?\,({object}[^\,]+)?"""
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
"""\:\d{2}\,(|({host}[^\,]+))\,(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\,(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?),(|({connection_id}\d+))\,(|({query_id}\d+))\,(|({db_operation}\w+))\,(|({db_name}[^\,]+))\,(|({object}[^\,]+)),"""
]
ParserVersion = "v1.0.0"
},

${MongoDBParserTemplates.mongodb-database-events}{
  Name = "mongodb-m-json-database-modify-success-createcollection"
  Conditions = [ """"atype" :""", """"createCollection"""", """"ts"""", """"local" : {""", """"param" :""", """"users" : [""" ]
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
  """"ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
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
  """exa_json_path=$.ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
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

${GoAnywhereParsersTemplates.goanywhere-events-2}{
  Name = goanywhere-gamft-kv-endpoint-login-success-loginsuccessful-1
  Conditions = [ """GoACHevent_type="Login Successful"""", """GoACHcommand="Login"""", """GoACHremote_ip="""", """GoACHuser_name="""" ]
  ParserVersion = v1.0.0
},

${GoAnywhereParsersTemplates.goanywhere-events-2}{
  Name = goanywhere-gamft-kv-endpoint-login-success-connectionsuccessful-1
  Conditions = [ """GoACHevent_type="Connection Successful"""", """GoACHcommand="Connect"""", """GoACHremote_ip="""", """GoACHremarks="Connection established"""" ]
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
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
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
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
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
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
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

{
Vendor = "Apache"
Product = "Cassandra db"
TimeFormat = "epoch"
Fields = [
  """\|timestamp\:({time}\d{13})"""
  """\-\shost:\/({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\|source:\/({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
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
Name = mariadb-m-csv-database-login-success-connect-1
Vendor = "MariaDB"
Product = "MariaDB"
TimeFormat = "yyyyMMdd HH:mm:ss"
Conditions = [
  """ mariadb """
  """,CONNECT,"""
]
Fields = [
  """ mariadb ({time}\d{1,8} \d\d:\d\d:\d\d),"""
  """\:\d{2}\,(|({host}[^\,]+))\,(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\,(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?),(|({connection_id}\d+))\,(|({query_id}\d+))\,(|({db_operation}\w+))\,(|({db_name}[^\,]+))\,(|({object}[^\,]+)),"""
]
ParserVersion = "v1.0.0"
},

{
  Name = postgresql-p-csv-database-login-success-authentication
  Vendor = PostgreSQL
  Product = PostgreSQL
  TimeFormat = ["yyyy-MM-dd HH:mm:ss.SSS","yyyy-MM-dd HH:mm:ss"]
  Conditions = [ """connection authorized:""", """ user=""", """ database=""", """LOG""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s*UTC"""
    """({time}\d{4}-\d{2}-\d{2}\s(\d{2}:){2}\d{2}\.\d{3,})\sUTC""",
    """({additional_info}({action}connection authorized):\s*(\[[^\]]+\]:|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)?\s*user=({db_user}[^=]+?)(\sdatabase=({db_name}[^"\s=]+))?("|\s)(application_name=({app}[^\s]+)\s)?[^"]*)("|$)*"""
    """database=({db_name}[\w\.\-]+)"""
    """:LOG:\s*({action}[^:]+)"""
  ]
  ParserVersion = "v1.0.0"
  DupFields = ["db_user -> user"
}
```