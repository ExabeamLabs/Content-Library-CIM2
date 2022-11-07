#### Parser Content
```Java
{
Name = ibm-guardium-kv-database-query-success-dbuser
Vendor = "IBM"
Product = "Infosphere Guardium"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """SQLID="""
  """AppUserName ="""
  """DB_NAME="""
  """DBUser="""
]
Fields = [
  """({host}[\w.\-]+)\s+\w+\[.*?\]:\s*AppUserName ="""
  """\WreceiptTime=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
  """\WAppUserName =PLAN=({user}[^;\|]+?)\s*(?:;|\||$)"""
  """\WPROG=({src_program}[^;\|]+?)\s*(?:;|\||$)"""
  """\WDB_NAME=({db_name}[^;\|]+?)\s*(?:;|\||$)"""
  """\WclientHostname=({src_host}[^;\|]+?)\s*(?:;|\||$)"""
  """\WclientIP=({src_ip}[a-fA-F\d.:]+)"""
  """\WclientPort=({src_port}\d+)"""
  """\WDBProtocol=({db_protocol}[^;\|]+?)\s*(?:;|\||$)"""
  """\WDBUser=({db_user}[^;\|]+?)\s*(?:;|\||$)"""
  """\WruleDescription=({rule_description}[^;\|]+?)\s*(?:;|\||$)"""
  """\WserverType=({server_group}[^;\|]+?)\s*(?:;|\||$)"""
  """\WserviceName =({service_name}[^;\|]+?)\s*(?:;|\||$)"""
  """\WVerb=({db_operation}[^;\|]+?)\s*(?:;|\||$)"""
]
DupFields = [
  "db_user->account"
]
ParserVersion = "v1.0.0"


}
```