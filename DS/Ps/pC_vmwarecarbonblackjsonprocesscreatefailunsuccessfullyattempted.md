#### Parser Content
```Java
{
Name = "vmware-carbonblack-json-process-create-fail-unsuccessfullyattempted"
Conditions = [
  """threatIndicators"""
  """"eventType":"SYSTEM_API_CALL""""
  """unsuccessfully attempted"""
]
ParserVersion = "v1.0.0"

carbonblack-edr.Fields}[
    """"parent_path":"({parent_process_path}({parent_process_dir}[^"]+(\\|\/)+)?({parent_process_name}[^"]+))""""
}
```