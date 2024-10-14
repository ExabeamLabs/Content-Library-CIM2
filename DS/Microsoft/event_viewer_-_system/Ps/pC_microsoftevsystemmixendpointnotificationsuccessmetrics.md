#### Parser Content
```Java
{
Name = microsoft-evsystem-mix-endpoint-notification-success-metrics
  Vendor = Microsoft
  Product = Event Viewer - System
  TimeFormat = "epoch_sec"
  Conditions = [ """source="""", """"host":"""", """ edge_fleet="""" ]
  Fields = [
    """"_time":({time}\d{10})""",
    """"host":"({host}[\w\-.]+)"""",
    """({log_source}metrics)""",
    """edge_host="({edge_host}[^"]+)"""
    """edge_source="({log_source}[^"]+)"""
    """edge_fleet="({edge_fleet}[^"]+)"""
    """windows_cpu_percent_all_total":({cpu_percentile}\d+),"""
    """windows_cpu_time_total":({cpu_percentile}\d+)"""
    """"process_pid":({process_id}\d+)"""
    """"host":[^,]+,({additional_info}[^\}]+)\}"""
    """process_handles":({handle_id}[^,]+),"""
    """process_threads":({thread_id}[^,]+),"""
    """process_page_faults_total":({page_fault_count}\d+),"""
    """process_cpu_time_total":({cpu_percentile}[^,]+),"""
    """windows_logical_disk_size_bytes":({disk_size}[^,]+),"""
  ]
  ParserVersion = v1.0.0


}
```