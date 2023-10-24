#### Parser Content
```Java
{
Name = buildkite-bk-json-app-notification-success-triggerjob
  ParserVersion = v1.0.0
  Conditions = [ """"pipeline":""", """"source":"trigger_job"""", """"created_at":""", """"cribl_pipe":"buildkite-job-scheduled-events"""" ]
 
buildkite-app-activity = {
  Vendor = Buildkite
  Product = Buildkite
  TimeFormat = "epoch_sec"
  Fields = [
    """"\_time":({time}\d{10})"""
    """"web_url":"({url}(\w+:\/\/)?({web_domain}[^"\\\/:]+)(:({dest_port}\d+))?({uri_path}[\\\/]+[^"\?]*?)({uri_query}\?[^"]*)?)""""
    """"repository":"({repository_name}[^"]+)""""
    """"default_branch":"({branch_name}[^"]+)""""
    """"build":\{"creator".+?,"name":"({full_name}[^"]+)"""
    """"build":\{"creator".+?,"email":"({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
    """"job":[^\}]+?"id":"({task_id}[^"]+)""""
    """"job":[^\}]+?"name":"({task_name}[^"]+)""""
    """"meta_data":\{({additional_info}[^\}]+)"""
    """({app}buildkite)"""
    ] 
   
}
```