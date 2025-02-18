#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-network-session-success-5158"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["EEE MMM dd HH:mm:ss yyyy", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
Conditions = [
  """5158"""
  """The Windows Filtering Platform has permitted a bind to a local port"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
  """\d+\s*\d+:\d+:\d+\s+(::ffff:)?(am|pm|\d{4}|({host}[\w\-.]+))\s"""
  """<TimeCreated SystemTime\\*=('|")?({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,9})?Z)"""
  """({time}\w+ \w+ \d\d \d\d:\d\d:\d\d \d\d\d\d)\s+"""
  """({event_code}5158)"""
  """\WComputer\\*=(::ffff:)?({host}[\w\-.]+)"""
  """Computer(Name)?\s*\\*\"?(=|:|>)\s*\"*(::ffff:)?({host}[\w\.-]+)(\s|,|\"|</Computer>|$)"""
  """({event_name}The Windows Filtering Platform has permitted a bind to a local port)"""
  """Process ID:\s*({process_id}\d+)"""
  """Application Name:.+?\s*(({process_path}(({process_dir}[^"\/:]*)\\)?({process_name}[^":]+?)))\s*Network Information:"""
  """Source Address:\s*(0\.0\.0\.0|(::ffff:)?({src_ip}(?!::)[a-fA-F:\d.]+))?.*?\s*Source Port:\s*({src_port}\d*)"""
  """Protocol:\s*({ms_protocol_num}\d*)"""
  """Layer Name:\s*({layer_name}.*?)\s*Layer Run-Time ID"""
]
DupFields = [
  "host->src_host", "ms_protocol_num->protocol"
]
ParserVersion = "v1.0.0"


}
```