#### Parser Content
```Java
{
Name = "vmware-carbonblack-json-process-create-success-invoked"
Conditions = [
  """threatIndicators"""
  """invoked"""
  """eventType":"CREATE_PROCESS"""
  """destinationServiceName =CB Defense"""
  """dproc=create process event"""
]
ParserVersion = "v1.0.0"

carbonblack-edr.Fields}[
    """"parent_path":"({parent_process_path}({parent_process_dir}[^"]+(\\|\/)+)?({parent_process_name}[^"]+))""""
}
```