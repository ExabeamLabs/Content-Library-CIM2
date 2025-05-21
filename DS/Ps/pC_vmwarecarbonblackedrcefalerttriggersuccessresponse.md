#### Parser Content
```Java
{
Name = "vmware-carbonblackedr-cef-alert-trigger-success-response"
Conditions = [
  """CEF:"""
  """|CarbonBlack|Response|"""
  """watchlist.storage.hit.process"""
]
ParserVersion = "v1.0.0"

carbonblack-edr.Fields}[
    """"parent_path":"({parent_process_path}({parent_process_dir}[^"]+(\\|\/)+)?({parent_process_name}[^"]+))""""
}
```