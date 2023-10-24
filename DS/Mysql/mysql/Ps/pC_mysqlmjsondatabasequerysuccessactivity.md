#### Parser Content
```Java
{
Name = "mysql-m-json-database-query-success-activity"
Vendor = "Mysql"
Product = "Mysql"
TimeFormat = "epoch"
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
""""os_user":"({user}[\w\.\-]{1,40}\$?)""""
""""status":"({action}[^"]+)""""
""""cmd":"({db_operation}[^"]+)""""
""""db":"({db_name}[^"]+)""""
""""name":"({db_object}[^"]+)""""
""""query":"({db_query}[^"]+)""""
]
DupFields = [
"dest_host->host"
]
ParserVersion = "v1.0.0"


}
```