#### Parser Content
```Java
{
Name = tanium-ep-kv-process-create-success-cliexecutionlog
    Vendor = Tanium
    Product = Endpoint Platform
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSZ"
    Conditions = [ """exabeam_sourcetype=tanium:cli_execution_log""" ]
    Fields = [
      """({operation_type}cli_execution)""",
    ]
    DupFields = [ "host->dest_host","path->process_path","directory->process_dir" ]
  

}
```