#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-notification-success-multipathd
  Conditions = [ """multipathd[""", """: sda: """, """: failed to get """, """ uid: """ ]
  Fields = ${DLUnixParserTemplates.unix-system-info.Fields}[
    """:\ssda:\sfailed[^:]+?:\s({failure_reason}[^"$]+?)\s*$""",
    """:\ssda:\s({event_name}[^:]{1,2000})"""
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]
  ParserVersion = "v1.0.0"

unix-system-info = {
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """(multipathd|avahi-daemon)\[\d+\]:(\ssda:)?\s({additional_info}[^"$]+?)\s*$"""
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s+"""
  
}
```