#### Parser Content
```Java
{
Name = cyberark-pam-kv-file-write-success-storefile
Conditions = [
  """%CYBERARK:"""
  """Message="Store File"""
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