#### Parser Content
```Java
{
Name = buildkite-bk-json-app-notification-success-triggerjob
  ParserVersion = v1.0.0
  Conditions = [ """"pipeline":""", """"source":"trigger_job"""", """"created_at":""", """"cribl_pipe":"buildkite-job-scheduled-events"""" ]
 
buildkite-app-activity = {
  Vendor = Buildkite
  Product = Buildkite
  ExtractionType = json
  TimeFormat = "epoch_sec"
  Fields = [
    """exa_regex="\_time":({time}\d{10})"""
    """exa_json_path=$.pipeline,exa_regex="web_url":"({url}(\w+:\/\/)?({web_domain}[^"\\\/:]+)(:({dest_port}\d+))?({uri_path}[\\\/]+[^"\?]*?)({uri_query}\?[^"]*)?)""""
    """exa_json_path=$.pipeline.repository,exa_field_name=repository_name"""
    """exa_json_path=$.pipeline.default_branch,exa_field_name=branch_name"""
    """exa_json_path=$.job.name,exa_field_name=full_name"""
    """exa_json_path=$.job.agent.name,exa_field_name=full_name"""
    """exa_json_path=$.build.creator.name,exa_field_name=full_name"""
    """exa_json_path=$.build.author.email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""    
    """exa_json_path=$.build.creator.email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
    """exa_json_path=$.job.id,exa_field_name=task_id"""
    """exa_json_path=$.job.agent.id,exa_field_name=task_id"""
    """exa_json_path=$.job.name,exa_field_name=task_name"""
    """exa_json_path=$.job.agent.name,exa_field_name=task_name"""
    """exa_json_path=$.build.meta_data,exa_regex=\{({additional_info}[^\}]+)"""
    """exa_regex=({app}buildkite)"""
    ] 
   
}
```