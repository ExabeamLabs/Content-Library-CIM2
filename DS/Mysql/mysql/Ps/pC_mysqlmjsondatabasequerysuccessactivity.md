#### Parser Content
```Java
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


}
```