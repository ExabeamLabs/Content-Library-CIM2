#### Parser Content
```Java
{
Name = unix-unix-str-dns-record-create-success-registeringnewaddress
  Conditions = [ """avahi-daemon[""", """]: Registering new address record for""" ]
  Fields = ${DLUnixParserTemplates.unix-system-info.Fields}[
    """Registering new address record for\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """({event_name}Registering new address record)"""
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