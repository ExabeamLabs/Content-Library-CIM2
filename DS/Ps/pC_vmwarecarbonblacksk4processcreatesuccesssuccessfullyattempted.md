#### Parser Content
```Java
{
Name = "vmware-carbonblack-sk4-process-create-success-successfullyattempted"
Conditions = [
  """threatIndicators"""
  """eventType":"SYSTEM_API_CALL"""
  """ successfully attempted """
]
ParserVersion = "v1.0.0"

carbonblack-edr.Fields}[
    """"parent_path":"({parent_process_path}({parent_process_dir}[^"]+(\\|\/)+)?({parent_process_name}[^"]+))""""
}
```