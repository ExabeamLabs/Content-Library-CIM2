#### Parser Content
```Java
{
Name = microsoft-evadfs-kv-endpoint-activity-success-1644
  Vendor = Microsoft
  Product = Event Viewer - ADFS
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """1644""", """A client issued a search operation with the following options""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+)\S*\s+({host}[\w\-.]+)\s+EvntSLog""",
    """({event_code}1644)""",
    """({event_name}A client issued a search operation with the following options)""",
    """Client:\s*({src_ip}[A-Fa-f:\d.]+?):({src_port}\d+)\s""",
    """Filter:\s*({filter}.*?)\s+Search scope:""",
    """Search scope:\s*({search_scope}.*?)\s+Attribute selection:""",
    """Attribute selection:\s*\[?({attribute_selection}[^\]]*?)\]?\s+Server controls:""",
    """Server controls:\s*(|({server_controls}.*?))\s+Visited entries:""",
    """Visited entries:\s*({valid_entries}\d+)""",
    """Returned entries:\s*({returned_entries}\d+)""",
    """Used indexes:\s*Ancestors_index:\s*({used_indexes}.*?);\s*Pages referenced:""",
    """Pages referenced:\s*({pages_referenced}\d+)""",
    """Pages read from disk:\s*({pages_read_from_disk}\d+)""",
    """Pages preread from disk:\s*({pages_preread_from_disk}\d+)""",
    """Clean pages modified:\s*({clean_pages_modified}\d+)""",
    """Dirty pages modified:\s*({dirty_pages_modified}\d+)""",
    """Search time \(ms\):\s*({search_time}\d+)""",
    """Attributes Preventing Optimization:\s*({attributes_preventing_optimization}.*?)\s+User:""",
    """User:\s*(({domain}[^\\\s"]+)\\+)?({user}[^\\\s"]+)""",
  ]


}
```