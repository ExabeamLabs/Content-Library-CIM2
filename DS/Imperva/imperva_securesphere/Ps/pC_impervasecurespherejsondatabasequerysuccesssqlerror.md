#### Parser Content
```Java
{
Name = imperva-securesphere-json-database-query-success-sqlerror
Vendor = "Imperva"
Product = "Imperva SecureSphere"
TimeFormat = "dd MMMM yyyy HH:mm:ss z"
Conditions = [
  """"Imperva Inc.|SecureSphere|"""
  """|Audit|Audit.DAM|"""
  """"db-user""""
  """"event-type""""
  """"sql-error""""
]
Fields = [
  """"+real-time"+\s*:\s*"+(?:|({time}.[^"]+))"+(,|})"""
  """"audit-policy":\s*\[\s*"(|({policy_name}[^\]"]+))"\s*\]"""
  """"+gw-ip"+\s*:\s*"+(?:|({host}[^"]+))"+(,|})"""
  """"+dest-ip"+\s*:\s*"+(?:|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"+(,|})"""
  """"+source-ip"+\s*:\s*"+(?:|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"+(,|})"""
  """"+db-user"+\s*:\s*"+(?:|({domain}[^"]+))"+(,|})"""
  """"+db-user"+\s*:\s*"+(?:|({user}[^"\\@]+?)(@({domain}[^"]+))?)"+(,|})"""
  """"+db-user"+\s*:\s*"+(?:|({domain}[^"\\@]+?)(\\+({user}[^"]+))?)"+(,|})"""
  """"+event-type"+\s*:\s*"+(?:|({event_category}[^"]+))"+(,|})"""
  """"+application-name"+\s*:\s*"+(?:|({app}[^"]+))"+(,|})"""
  """"+service-name"+\s*:\s*"+(?:|({service_name}[^"]+))"+(,|})"""
  """"+server-group"+\s*:\s*"+(?:|({server_group}[^"]+))"+(,|})"""
  """({db_name}db)"+(,|})"""
  """"+db-name"+\s*:\s*"+(?:|({db_name}[^"]+))"+(,|})"""
  """"+schema-name"+\s*:\s*"+(?:|({db_schema}[^"]+))"+(,|})"""
  """"+sql-error"+\s*:\s*"+(?:|({sql_error}[^"]+))"+(,|})"""
  """"+raw-query"+\s*:\s*"+[\\r\s]*(?:|({db_query}[^",].+?[^\\]))\s*"+(,\s*"+|})"""
  """"+parsed-query"+\s*:\s*"+(?:(N\\\/A \((logout|login)\))|(?:|({db_query}.*?[^\\])))\s*"+(,\s*"+|})"""
  """"+raw-query"+\s*:\s*"+[\\r\s]*(?:|({db_operation}[^,"]\S+).*?[^\\])\s*"+(,\s*"|})"""
  """"+parsed-query"+\s*:\s*"+(?:(N\\\/A)|({db_operation}\S+)).+?[^\\]\s*"+(,\s*"+|})"""
  """"user-group"\s*:\s*"(|({user_group_name}[^"]+))""""
  """"application-user"\s*:\s*"(|({app_user}[^"]+))""""
  """"host-name"\s*:\s*"({host}[\w\-.]+)""""
  """"policy-id"\s*:\s*\[\s*"({policy_id}[^"]+)""""
]
DupFields = [
  "user->account"
  "user->db_user"
]
ParserVersion = "v1.0.0"


}
```