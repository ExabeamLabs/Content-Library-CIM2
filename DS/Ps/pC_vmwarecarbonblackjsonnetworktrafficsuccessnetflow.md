#### Parser Content
```Java
{
Name = "vmware-carbonblack-json-network-traffic-success-netflow"
Conditions = [
  """threatIndicators"""
  """eventType":"NETWORK"""
  """destinationServiceName =CB Defense"""
  """processDetails":""""
  """netFlow"""
  """successful"""
]
ParserVersion = "v1.0.0"

carbonblack-edr.Fields}[
    """"parent_path":"({parent_process_path}({parent_process_dir}[^"]+(\\|\/)+)?({parent_process_name}[^"]+))""""
}
```