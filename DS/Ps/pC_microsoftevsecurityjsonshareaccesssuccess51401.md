#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-share-access-success-5140-1"
Conditions = [
  """"event_id":5140"""
  """Microsoft-Windows-Security-Auditing"""
  """A network share object was accessed"""
]
ExtractionType = json
ParserVersion = "v1.0.0"

microsoft-json-events.Fields}[
    """exa_json_path=$.Computer,exa_field_name=host""",
		"""exa_json_path=$.UserID,exa_regex=(({user_sid}S-[^"]+?)|(({domain}[^"]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
		"""exa_regex=Account Name:\s*(({domain}[^:\\]+?)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+){1,2}:\s""",
    """exa_regex=Account Domain:\s+({domain}[^\s]+)""",
    """exa_regex=Share Information:\s+Object Type:\s+({file_type}[^:]+?)\s+Share Name:""",
    """exa_regex=Share Name:\s+(?:[\\\*]+)?({share_name}[^\s]+)\s+Share Path:""",
    """exa_regex=Share Path:\s*[\\\?]*({share_path}(({d_parent}[^@]+?)\\)?(|({d_name}[^\\]+?)))\s*Old Remark:"""
  
}
```