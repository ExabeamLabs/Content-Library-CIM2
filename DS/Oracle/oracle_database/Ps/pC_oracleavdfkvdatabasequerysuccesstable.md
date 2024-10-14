#### Parser Content
```Java
{
Name = "oracle-avdf-kv-database-query-success-table"
Conditions = [
""" TARGET_TYPE="TABLE""""
""" SECURED_TARGET_NAME=""""
""" SECURED_TARGET_TYPE=""""
]
ParserVersion = "v1.0.0"

oracle-db-template-2.Fields}[
     """sql\.COMMENT_TEXT="({additional_info}[^@]+?)"\s+[\w\.]+?="""
   ]
 },

{
Name = oracle-o-kv-database-login-success-dbx
Vendor = "Oracle"
Product = "Oracle Database"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
Conditions = [
  """SESSIONID="""
  """Authenticated by"""
  """DBID="""
]
Fields = [
  """NTIMESTAMP\#="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)"""
  """USERID="({db_user}[^"]+)"""
  """USERHOST="({src_host}[^"]+)"""
  """RETURNCODE="({result}[^"]+)"""
  """Client address.+?\(PROTOCOL=({protocol}[^\)]+)"""
  """Client address.+?\(HOST=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """SPARE1="({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
]
DupFields = [
  "db_user->account"
]
ParserVersion = "v1.0.0"
},
 
{
Name = oracle-db-xml-database-login-success-dbauth
Vendor = "Oracle"
Product = "Oracle Database"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
  """<DB_User>"""
  """<OS_User>"""
  """<Userhost>"""
  """<OS_Process>"""
  """Authenticated by:"""
]
Fields = [
  """<Extended_Timestamp>({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+\w)</Extended_Timestamp>"""
  """<DB_User>(\/|({db_user}.+?))</DB_User>"""
  """<OS_User>({user}[\w\.\-\!\#\^\~]{1,40}\$?)</OS_User>"""
  """<Userhost>({src_host}[^\<]+)</Userhost>"""
  """<OS_Process>({process_id}\d+)</OS_Process>"""
  """<Session_Id>({session_id}\d+)</Session_Id>"""
  """<Returncode>({result}.+?)</Returncode>"""
  """<DBID>({db_name}.+?)</DBID>"""
  """PROTOCOL=({protocol}[^\)]+)"""
  """HOST=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """PORT=({src_port}\d+)"""
]
DupFields = [
  "user->user"
  "db_user->account"
]
ParserVersion = "v1.0.0"
},
   
${OracleParsersTemplates.oracle-db-template-2} {
   Name = oracle-db-kv-database-activity-success-grant
   Conditions = [ """.sql.AUDIT_TYPE="Standard Audit"""", """.sql.STATEMENT_TYPE="GRANT""", """.sql.DB_USER=""", """.sql.USERHOST=""" ]
   Fields = ${OracleParsersTemplates.oracle-db-template-2.Fields}[
    """sql\.OBJ_PRIVILEGE=({privileges}[^=]+?)\s+[\w\.]+?=""",
    """sql\.STATEMENT_TYPE=({db_operation}[^=]+?)\s+[\w\.]+?="""
   ]
   ParserVersion = "v1.0.0"
 },

{
Name = "oracle-db-cef-database-delete-success-delete"
Vendor = "Oracle"
Product = "Oracle Database"
TimeFormat = "epoch"
Conditions = [
"""|Oracle|FGA|"""
"""|DELETE|"""
]
Fields = [
"""\Wrt=({time}\d{13})"""
"""\Wshost=({src_host}[\w\-.]+)"""
"""\Wdhost=({dest_host}[\w\-.]+)"""
"""\Wsuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""\Wduser=({db_user}[^\s]+)"""
"""\Wcs3=({db_name}[^\s]+)"""
"""CEF:([^\|]*\|){5}({db_operation}[^\|]+)"""
]
DupFields = [
"db_user->account"
]
ParserVersion = "v1.0.0"
},

{
Vendor = "Oracle"
Product = "Oracle Database"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Fields = [
"""exa_json_path=$.timestamp,exa_field_name=time"""
"""exa_json_path=$.userhost,exa_regex=(({domain}[^\\]+)[\\]+)?({src_host}[^"]+)"""
"""exa_json_path=$.os_username,exa_field_name=user"""
"""exa_json_path=$.username,exa_field_name=db_user"""
"""exa_json_path=$.db_name,exa_field_name=db_name"""
"""exa_json_path=$.sessionid,exa_field_name=session_id"""
"""exa_json_path=$.priv_used,exa_field_name=additional_info"""
"""exa_json_path=$.exa_jdbc_hostname,exa_field_name=dest_host"""
"""exa_json_path=$.exa_jdbc_database,exa_field_name=db_name"""
"""exa_regex=({db_operation}---S------------)"""
"""exa_json_path=$.action_name,exa_field_name=db_operation""""
"""exa_regex=({event_name}SESSION REC)"""
"""exa_json_path=$.obj_name,exa_field_name=db_object"""
"""exa_json_path=$.exa_jdbc_type,exa_field_name=app"""
"""exa_json_path=$.exa_jdbc_port,exa_field_name=dest_port"""
"""exa_json_path=$.returncode,exa_field_name=return_code"""
"""exa_json_path=$.terminal,exa_field_name=terminal"""
]
DupFields = [
"user->user"
"db_user->account"
]
Name = "oracle-db-json-database-delete-success-sessionrec"
ExtractionType = json
Conditions = [
""""action_name":"SESSION REC""""
""""ses_actions":"---S------------""""
""""exa_jdbc_type":"""
""""Oracle""""
]
ParserVersion = "v1.0.0"
},

${OracleParsersTemplates.oracle-db-template-2} {
   Name = "oracle-db-kv-database-modify-success-update"
   Conditions = [ """.sql.AUDIT_TYPE="Standard Audit"""", """.sql.STATEMENT_TYPE=UPDATE""", """.sql.DB_USER=""", """.sql.USERHOST=""" ]
   Fields = ${OracleParsersTemplates.oracle-db-template-2.Fields}[
     """sql\.STATEMENT_TYPE=({db_operation}[^=]+?)\s+[\w\.]+?="""
   ]
   ParserVersion = "v1.0.0"
 },


{
Vendor = "Oracle"
Product = "Oracle Audit Vault and Database Firewall"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Fields = [
"""EVENT_TIME="({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""
"""SECURED_TARGET_NAME="({host}[^-]+)-({db_name}[^"]+)""""
"""USER_NAME="(unknown_username|({db_user}[^"]+))""""
"""OSUSER_NAME="(({domain}[^\\]+)\\)?((?i)system|unknown_osusername|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
"""CLIENT_HOST_NAME="({src_host}[^"]+)""""
"""CLIENT_IP="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
"""EVENT_NAME="({event_name}[^"]+)""""
"""RECORD_ID="({event_code}[^"]+)""""
"""SECURED_TARGET_TYPE="({app}[^"]+)""""
"""SERVICE_NAME="(unknown_service|({db_name}[^"]+))""""
"""TARGET_OBJECT="({table_name}[^"]+)""""
"""COMMAND_CLASS="({db_operation}[^"]+)""""
"""COMMAND_TEXT="(\s+|({db_query}[^"]+?))\s*("|$)"""
]
Name = "oracle-avdf-kv-database-query-success-table"
Conditions = [
""" TARGET_TYPE="TABLE""""
""" SECURED_TARGET_NAME=""""
""" SECURED_TARGET_TYPE=""""
]
ParserVersion = "v1.0.0"
},

${OracleParsersTemplates.oracle-db-template-2} {
   Name = oracle-db-str-database-query-success-insert
   ParserVersion = "v1.0.0"
   Conditions = [ """.sql.AUDIT_TYPE="Standard Audit"""", """.sql.STATEMENT_TYPE=INSERT""", """.sql.DB_USER=""", """.sql.USERHOST=""" ]
   Fields = ${OracleParsersTemplates.oracle-db-template-2.Fields}[
     """sql\.STATEMENT_TYPE=({db_operation}[^=]+?)\s+[\w\.]+?="""
   ]
 },

{
Name = "oracle-db-json-database-query-success-grantrole"
Vendor = "Oracle"
Product = "Oracle Database"
ExtractionType = json
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""os_username"""
""""dbid"""
""""sql_text"""
""""GRANT ROLE"""
]
Fields = [
    """exa_json_path=$..dbid,exa_field_name=db_id""",
    """exa_json_path=$..sql_text,exa_field_name=db_query""",
    """exa_json_path=$..userhost,exa_field_name=src_host""",
    """exa_json_path=$..terminal,exa_field_name=terminal""",
    """exa_json_path=$..timestamp,exa_field_name=time""",
    """exa_json_path=$..username,exa_field_name=db_user""",
    """exa_json_path=$..os_username,exa_field_name=user""",
    """exa_json_path=$..action_name,exa_field_name=db_operation"""
]
DupFields = [
"db_id->db_name"
"db_user->account"
]
ParserVersion = "v1.0.0"
},

{
Name = "oracle-db-json-database-query-success-oraclefga"
Vendor = "Oracle"
Product = "Oracle Database"
ExtractionType = json
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""OracleFGA""""
""""sqlText":"""
]
Fields = [
"""exa_json_path=$.objName,exa_field_name=db_object"""
"""exa_json_path=$.sqlText,exa_field_name=db_query"""
"""exa_json_path=$.objSchema,exa_field_name=db_schema"""
"""exa_json_path=$.@timestamp,exa_field_name=time"""
"""exa_json_path=$.srcHostname,exa_field_name=domain"""
"""exa_json_path=$.action,exa_field_name=db_operation"""
"""exa_json_path=$.instanceName,exa_field_name=db_name"""
"""exa_json_path=$.suUserID,exa_field_name=user"""
"""exa_json_path=$.userID,exa_field_name=db_user"""
]
ParserVersion = "v1.0.0"
},

${OracleParsersTemplates.oracle-db-template-2} {
   Name = oracle-db-kv-database-query-success-select
   ParserVersion = "v1.0.0"
   Conditions = [ """.sql.AUDIT_TYPE="Standard Audit"""", """.sql.STATEMENT_TYPE=SELECT""", """.sql.DB_USER=""", """.sql.USERHOST=""" ]
   Fields = ${OracleParsersTemplates.oracle-db-template-2.Fields}[
     """sql\.STATEMENT_TYPE=({db_operation}[^=]+?)\s+[\w\.]+?="""
   ]
 },
 
${OracleParsersTemplates.oracle-db-template-2} {
   Name = oracle-db-kv-database-query-success-createtable
   ParserVersion = "v1.0.0"
   Conditions = [ """.sql.AUDIT_TYPE="Standard Audit"""", """.sql.STATEMENT_TYPE="CREATE TABLE""", """.sql.DB_USER=""", """.sql.USERHOST=""" ]
   Fields = ${OracleParsersTemplates.oracle-db-template-2.Fields}[
     """sql\.STATEMENT_TYPE="({db_operation}[^=]+?) TABLE"\s+[\w\.]+?="""
   ]
 },
 
{
    Name = oracle-db-str-database-query-success-sysdba
    Vendor = Oracle
    Product = Oracle Database
    TimeFormat = ["MMM dd HH:mm:ss yyyy z","yyyy-MM-dd'T'HH:mm:ss.SSSSSS"]
    ParserVersion = "v1.0.0" 
    Conditions = [ """CLIENT USER:""", """PRIVILEGE :""", """ACTION :""", """'SYSDBA'""" ]
    Fields = [
      """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+)[-|+]\d+:\d\d\s*({host}[\w\-.]+)""",
      """\s({time}\w{3} \d\d \d\d:\d\d:\d\d \d\d\d\d [+-]\d\d:\d\d)""",
      """ACTION\s+:\[\d+\]\s+'\s*({db_query}({db_operation}\w+).*?)\s*'([\w\s]+\w+\s*:|$)""",
      """\sCLIENT USER:\[\d+\]\s*'({user}[\w\.\-\!\#\^\~]{1,40}\$?)'""",
      """\sDBID:\[\d+\]\s*'(|({db_name}[^']+))'""",
      """\sDATABASE USER:\[\d+\]\s*'(\/|({account}[^'\\\/\s]+))'""",
      """\sPRIVILEGE :\[\d+\]\s*'({privileges}[^']+)'""",
    ]
    DupFields = [ "user->user", "account->db_user" ]
 }

{
Name = oracle-pc-sk4-network-traffic-success-dataevent
Vendor = "Oracle"
Product = "Oracle Public Cloud"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  ""","type":"com.oraclecloud.vcn.flowlogs.DataEvent""""
  ""","flowid":""""
  ""","oracle":{""""
  """"compartmentid":""""
]
Fields = [
  """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""""
  """"sourceAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"sourcePort":({src_port}\d+)"""
  """"destinationAddress":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
  """"destinationPort":({dest_port}\d+)"""
  """"action":"({result}[^"]+)""""
  """"bytesOut":({bytes_out}\d+)"""
  """"protocolName":"({protocol}[^"]+)""""
]
ParserVersion = "v1.0.0"
},

{
   Name = oracle-db-kv-database-login-success-unifiedaudit
   Vendor = Oracle
   Product = Oracle Database
   ParserVersion = "v1.0.0"
   TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
   Conditions = [ """ACTION:"100"""", """DBUSER:"""", """DBID:"""", """Oracle Unified Audit"""]
   Fields = [
     """({host}[\w\-.]+)\s+(?:journal:)?\s+Oracle Unified Audit""",
     """DBID:\s*"+({db_name}\d+)""",
     """DBUSER:\s*"+({db_user}[^":]+)""",
     """CURUSER:\s*"+({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
     """ACTION:"({db_operation}100)"""",
     """RETCODE:"({return_code}\d+)""""
    ]
   DupFields = [ "db_name->db_id" ]
 },
 ${OracleParsersTemplates.oracle-public-cloud-events}{
  Name = oracle-pc-json-app-activity-success-appaccess
  ParserVersion = "v1.0.0"
  Conditions = [ """"ssoIdentityProvider":"""",""""eventId":"sso.app.access.success"""",""""serviceName":"SSO"""" 
}
```