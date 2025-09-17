#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-peripheral-storage-insert-success-enabledevice"
Conditions = [ """A device was enabled.""" ]
ParserVersion = "v1.0.0"

microsoft-json-events.Fields}[
    """exa_regex=Share Information:\s+Object Type:\s+({file_type}[^:]+?)\s+Share Name:""",
    """exa_regex=Share Name:\s+(?:[\\\*]+)?({share_name}[^\s]+)\s+Share Path:""",
    """exa_regex=Share Path:\s*[\\\?]*({share_path}(({d_parent}[^@]+?)\\)?(|({d_name}[^\\]+?)))\s*Old Remark:"""
  
}
```