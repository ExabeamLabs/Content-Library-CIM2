#### Parser Content
```Java
{
Name = cyberark-pam-kv-file-write-success-openfile
Conditions = [
  """%CYBERARK:"""
  """Message="Open File (Write Only)"""
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