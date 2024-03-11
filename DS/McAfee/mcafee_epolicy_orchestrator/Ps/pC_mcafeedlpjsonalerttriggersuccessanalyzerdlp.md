#### Parser Content
```Java
{
Name = mcafee-dlp-json-alert-trigger-success-analyzerdlp
	ParserVersion = v1.0.0
    Vendor = McAfee
    Product = McAfee ePolicy Orchestrator
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Conditions = [ """"analyzername":"Data Loss Prevention"""",""""threatname":""" ]
    Fields = [
      """"detectedutc":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
      """"db_ip":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """"threatname":"({alert_name}[^"]+?)"""",
      """"analyzername":"({alert_type}[^"]+?)"""",
      """"db_name":"({dest_host}[^"]+?)"""",
      """"sourcehostname":"({src_host}[^"]+?)"""",
      """"sourceprocessname":"({process_path}(({process_dir}[^"]*?)\\)?({process_name}[^"\\]*?))"""",
      """"threatactiontaken":"({action}[^"]+?)"""",
      """"sourceusername":"(({domain}[^"\\\/]+?)[\\\/]+)?({user}[^"]+)""""
    ]
    DupFields = [ "src_host->host" ]
  

}
```