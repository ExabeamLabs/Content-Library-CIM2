#### Parser Content
```Java
{
Name = "cyberark-epm-str-alert-trigger-success-detected"
Vendor = "CyberArk"
Product = "CyberArk Endpoint Privilege Manager"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """ThreatDetectionAction"""
  """: Detected"""
  """Computer"""
  """PolicyName"""
  """ProcessCertificateIssuer"""
  """SourceProcessCertificateIssuer"""
]
Fields = [
  """PolicyName\s+:\s*({alert_name}[^\]]+?)\s+\w+\s+:"""
  """Computer\s+:\s*({host}[^\s]+)"""
  """SourceProcessCommandLine\s+:\s*({parent_process_path}[^]]+?)\s+\w+\s+:"""
  """\sProcessCommandLine\s+:\s*({process_command_line}[^]]+?)\s+\w+\s+:"""
  """FilePath\s+:\s*({process_path}({process_dir}[^=]+\\)([^=]*?)?)\s+\w+\s+:"""
  """Hash\s+:\s*({hash_sha256}\S+)"""
  """FileName\s+:\s*({file_name}[^]]+?)\s+\w+\s+:"""
  """User\s+:\s*((?i)eis)?(.\\|\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """PolicyCategory\s+:\s*({alert_type}[^]]+?)\s+\w+\s+:"""
  """FilePath\s+:\s*({file_path}[^]]+?)\s+\w+\s+:"""
]
DupFields = [
  "host->dest_host"
  "file_name->process_name"
  "file_path->path"
]
ParserVersion = "v1.0.0"


}
```