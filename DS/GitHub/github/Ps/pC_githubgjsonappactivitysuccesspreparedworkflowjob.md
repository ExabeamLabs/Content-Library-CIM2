#### Parser Content
```Java
{
Name = github-g-json-app-activity-success-preparedworkflowjob
  ParserVersion = "v1.0.0"
  ExtractionType = json
  Conditions = [ """"action":""", """"workflows.prepared_workflow_job"""", """"operation_type":""", """"modify"""" ]
  Fields = ${GithubParsersTemplates.json-github-actions.Fields} [
    """"job_name":"({additional_info}[^"]+)""",
    """"job_workflow_ref":"({object}[^"]+)""",
    """exa_json_path=$..job_name,exa_field_name=additional_info""",
    """exa_json_path=$..job_workflow_ref,exa_field_name=object"""
  ]

json-github-actions = {
    Vendor = GitHub
    Product = GitHub
    TimeFormat = "epoch"
    Fields = [
      """"@timestamp":\s*({time}\d{13})""",
      """"action":\s*"({operation}[^"]+)""",
      """"transport_protocol_name":\s*"({protocol}[^"]+)""",
      """"user_agent":\s*"({user_agent}[^"]+)""",
      """"actor_ip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """"repo":\s*"({object}[^"]+)""",
      """"actor":\s*"({user}[\w\.\-]{1,40}\$?)""",
      """"user":\s*"({user}[\w\.\-]{1,40}\$?)""",
      """"operation_type":\s*"({operation_type}[^"]+)""",
      """({app}(?i)github)""",
      """"key":\s*"({key_name}[^"]+)"""",
      """exa_json_path=$..['@timestamp'],exa_field_name=time""",
      """exa_json_path=$..action,exa_field_name=operation""",
      """exa_json_path=$..transport_protocol_name,exa_field_name=protocol""",
      """exa_json_path=$..user_agent,exa_field_name=user_agent""",
      """exa_json_path=$..actor_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """exa_json_path=$..repo,exa_field_name=object""",
      """exa_json_path=$..actor,exa_regex=({user}[\w\.\-]{1,40}\$?)""",
      """exa_json_path=$..user,exa_regex=({user}[\w\.\-]{1,40}\$?)""",
      """exa_json_path=$..operation_type,exa_field_name=operation_type""",
      """exa_json_path=$..key,exa_field_name=key_name""",
      """exa_json_path=$.['@timestamp'],exa_field_name=time""",
      """exa_json_path=$.action,exa_field_name=operation""",
      """exa_json_path=$.transport_protocol_name,exa_field_name=protocol""",
      """exa_json_path=$.user_agent,exa_field_name=user_agent""",
      """exa_json_path=$.actor_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """exa_json_path=$.repo,exa_field_name=object""",
      """exa_json_path=$.actor,exa_regex=({user}[\w\.\-]{1,40}\$?)""",
      """exa_json_path=$.user,exa_regex=({user}[\w\.\-]{1,40}\$?)""",
      """exa_json_path=$.operation_type,exa_field_name=operation_type""",
      """exa_json_path=$.key,exa_field_name=key_name""",
      """exa_regex=({app}(?i)github)"""
    
}
```