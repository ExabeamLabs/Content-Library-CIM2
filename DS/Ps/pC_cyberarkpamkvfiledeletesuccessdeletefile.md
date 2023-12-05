#### Parser Content
```Java
{
Name = cyberark-pam-kv-file-delete-success-deletefile
Conditions = [
  """%CYBERARK:"""
  """Message="Delete File""""
  """;Safe="""
]
DupFields = [
  "file_name->object_value"
  "file_path->additional_info"
  "operation->access"
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```