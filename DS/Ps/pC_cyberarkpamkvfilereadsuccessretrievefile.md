#### Parser Content
```Java
{
Name = cyberark-pam-kv-file-read-success-retrievefile
Conditions = [
  """%CYBERARK:"""
  """Message="Retrieve File"""
  """;Safe="""
]
DupFields = [
  "src_file_name->object_value"
  "src_file_path->additional_info"
  "operation->access"
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```