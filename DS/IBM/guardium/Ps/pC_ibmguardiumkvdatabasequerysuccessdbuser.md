#### Parser Content
```Java
{
Name = ibm-guardium-kv-database-query-success-dbuser
Vendor = "IBM"
Product = "Guardium"
TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss"]
Conditions = [
  """SQLID="""
  """AppUserName ="""
  """DB_NAME="""
  """DBUser="""
]
Fields = [
  """({time}\w+\s+\d+ \d+:\d+:\d+)"""
  """({host}[\w.\-]+)\s+\w+\[.*?\]:\s*AppUserName ="""
  """\WreceiptTime=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
  """\WAppUserName =PLAN=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*(?:;|\||$)"""
  """\WPROG=({src_interface}[^;\|]+?)\s*(?:;|\||$)"""
  """\WDB_NAME="?({db_name}[^;"\|]+?)\s*(?:;|"|\||$)"""
  """\WserverHostname="?({src_host}[^;\|"]+?)\s*(?:;|"|\||$)"""
  """\WclientIP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\WclientPort=({src_port}\d+)"""
  """\WDBProtocol=({app_protocol}[^;\|]+?)\s*(?:;|\||$)"""
  """\WDBUser="?({db_user}[^;\|"]+?)\s*(?:;|"|\||$)"""
  """\WruleDescription=({rule_description}[^;\|]+?)\s*(?:;|\||$)"""
  """\WserverType="?({server_group}[^;"\|]+?)\s*(?:;|"|\||$)"""
  """\WserviceName ="?({service_name}[^;"\|]+?)\s*(?:;|"|\||$)"""
  """\WVerb=({db_operation}[^;\|]+?)\s*(?:;|\||$)"""
]
DupFields = [
  "db_user->account"
]
ParserVersion = "v1.0.0"


}
```