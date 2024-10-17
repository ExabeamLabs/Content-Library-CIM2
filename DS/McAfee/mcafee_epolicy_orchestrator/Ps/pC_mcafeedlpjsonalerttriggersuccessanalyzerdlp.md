#### Parser Content
```Java
{
Name = mcafee-dlp-json-alert-trigger-success-analyzerdlp
    ExtractionType = json
	  ParserVersion = v1.0.0
    Vendor = McAfee
    Product = McAfee ePolicy Orchestrator
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Conditions = [ """"analyzername":"Data Loss Prevention"""",""""threatname":""" ]
    Fields = [
      """exa_json_path=$.detectedutc,exa_field_name=time"""
      """exa_json_path=$.db_ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
      """exa_json_path=$.threatname,exa_field_name=alert_name"""
      """exa_json_path=$.analyzername,exa_field_name=alert_type"""
      """exa_json_path=$.db_name,exa_field_name=dest_host"""
      """exa_json_path=$.sourcehostname,exa_field_name=src_host"""
      """exa_json_path=$.sourceprocessname,exa_regex=({process_path}(({process_dir}[^"]*?)\\)?({process_name}[^"\\]*?))$"""
      """exa_json_path=$.threatactiontaken,exa_field_name=result"""
      """exa_json_path=$.sourceusername,exa_regex=(({domain}[^"\\\/]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)$"""
    ]
    DupFields = [ "src_host->host" ]
  

}
```