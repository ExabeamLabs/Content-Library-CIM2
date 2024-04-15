#### Parser Content
```Java
{
Name = "sophos-ep-xml-alert-trigger-success-antivirus-tl"
    Vendor = "Sophos"
    Product = "Sophos Endpoint Protection"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "<provider name='sophos anti-virus'/>"
      "<eventdata><data>"
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d{3})"
      "(?i)<Computer>({src_host}.+?)</Computer>"
      "(?i)<EventData><Data>({alert_name}.+?)</Data><Data>({file_path}({file_dir}[^<>]+?)?({file_name}[^<>\\\\\\/]*?(\\.({file_ext}\\w+))?))(\\\\\\w+)?</Data><Data>.*?</Data><Data>({alert_type}.+?)</Data><Data>.*?</Data><Data>({result}.+?)\\.?\\s*</Data>"
      "(?i)<Computer>({src_host}.+?)</Computer>"
      "(?i)C:\\\\Users\\\\({user}[^\\\\<>]+)"
      "(?i)</Message><Level>({alert_severity}[^\\<]+)"
    ]
    ParserVersion = "v1.0.0"
  

}
```