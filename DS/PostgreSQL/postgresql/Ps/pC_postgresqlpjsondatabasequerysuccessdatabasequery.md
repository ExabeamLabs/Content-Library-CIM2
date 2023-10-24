#### Parser Content
```Java
{
Name = "postgresql-p-json-database-query-success-databasequery"
Vendor = "PostgreSQL"
Product = "PostgreSQL"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS z"
Conditions = [
""""connection_from":"""
""""error_severity":"""
""""session_line_num":"""
""""sql_state_code":"""
]
Fields = [
""""log_time":\s*"({time}[^"]+)""""
""""user_name":\s*"({user}[\w\.\-]{1,40}\$?)""""
""""database_name":\s*"({db_name}[^"]+)""""
""""process_id":\s*"({process_id}[^"]+)""""
""""connection_from":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""session_id":\s*"({session_id}[^"]+)""""
""""transaction_id":\s*"({transaction_id}[^"]+)""""
""""application_name":\s*"({app}[^"]+)""""
""""command":\s*"({db_operation}[^"]+)""""
""""statement":\s*"({db_query}[^"]+)""""
""""object_name":\s*"({db_object}[^"]+)""""
""""object_type":\s*"({object_type}[^"]+)""""
""""error_severity":\s*"({severity}[^"]+)""""
""""connection received:\s*host=({dest_host}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\sport=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
]
DupFields = [
"user->db_user"
]
ParserVersion = "v1.0.0"


}
```