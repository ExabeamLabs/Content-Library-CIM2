#### Parser Content
```Java
{
Name = imperva-securesphere-json-database-query-success-sqlerror
Vendor = "Imperva"
Product = "Imperva SecureSphere"
ExtractionType = json
TimeFormat = ["dd MMMM yyyy HH:mm:ss z","MMM dd yyyy HH:mm:ss z"]
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
  """"+dest-ip"+\s*:\s*"+(?:|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"+(,|})"""
  """"+source-ip"+\s*:\s*"+(?:|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"+(,|})"""
  """"+db-user"+\s*:\s*"+(?:|({domain}[^"]+))"+(,|})"""
  """"+db-user"+\s*:\s*"+(?:|({user}[\w\.\-]{1,40}\$?)(@({domain}[^"]+))?)"+(,|})"""
  """"+db-user"+\s*:\s*"+(?:|({domain}[^"\\@]+?)(\\+({user}[\w\.\-]{1,40}\$?))?)"+(,|})"""
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
  """exa_json_path=$.real-time,exa_field_name=time"""
  """exa_json_path=$.audit-policy,exa_regex=\s*\[\s*"(|({policy_name}[^\]"]+))"\s*\]"""
  """exa_json_path=$.gw-ip,exa_field_name=host"""
  """exa_json_path=$.dest-ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.source-ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.db-user,exa_regex=(?:|({domain}[^"\\@]+?)(\\+({user}[\w\.\-]{1,40}\$?))?)"+(,|})"""
  """exa_json_path=$.event-type,exa_field_name=event_category"""
  """exa_json_path=$.db-schema-pair.[0].db-name,exa_field_name=db_name"""
  """exa_json_path=$.sql-error,exa_regex=(?:|({sql_error}[^"]+))"""
  """exa_json_path=$.raw-query,exa_regex=(?:|({db_operation}[^"]+))"""
  """exa_json_path=$.parsed-query,exa_regex=(?:(N\\\/A)|({db_operation}\S+)).+?[^\\]\s*"+(,\s*"+|})"""
  """exa_json_path=$.user-group,exa_regex=(|({user_group_name}[^"]+))"""
  """exa_json_path=$.application-user,exa_regex=(|({app_user}[^"]+))"""
  """exa_json_path=$.host-name,exa_regex=({host}[\w\-.]+)"""
  """exa_json_path=$.policy-id,exa_regex=\s*\[\s*"({policy_id}[^"]+)"""
]
DupFields = [
  "user->account"
  "user->db_user"
]
ParserVersion = "v1.0.0"


}
```