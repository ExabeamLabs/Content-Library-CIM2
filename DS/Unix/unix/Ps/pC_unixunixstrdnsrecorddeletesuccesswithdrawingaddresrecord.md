#### Parser Content
```Java
{
Name = unix-unix-str-dns-record-delete-success-withdrawingaddresrecord
  Conditions = [ """avahi-daemon[""", """]: Withdrawing address record for """ ]
  Fields = ${DLUnixParserTemplates.unix-system-info.Fields}[
    """Withdrawing address record for\s({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """({event_name}Withdrawing address record)"""
  ]
  ParserVersion = "v1.0.0"

unix-system-info = {
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """(multipathd|avahi-daemon)\[\d+\]:(\ssda:)?\s({additional_info}[^"$]+?)\s*$"""
  
}
```