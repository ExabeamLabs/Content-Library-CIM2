#### Parser Content
```Java
{
Name = "mcafee-es-xml-file-write-success-epoevents-tl"
    ParserVersion = "v1.0.0"
    Vendor = "McAfee"
    Product = "McAfee Endpoint Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<scorevent_name>write_denied"
      "epoevents"
    ]
    Fields = [
      "(?i)<GMTTime>({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)</GMTTime>"
      "(?i)({host}[\\w\\-.]+)\\s+EPOEvents"
      "(?i)<SCORuser_name>(({domain}[^\\\\\\/<>]+)[\\\\\\/]+)?({user}[^\\\\\\/<>]+)</SCORuser_name>"
      "(?i)<SCORfile_name>({file_path}({file_dir}[^<>]*?[\\\\\\/<>]+)?({file_name}[^\\\\\\/<>]+?(\\.({file_ext}\\w+))?))</SCORfile_name>"
      "(?i)<SCORprocess_name>({process_path}({process_dir}[^<>]*?[\\\\\\/]+)?({process_name}[^\\\\\\/<>]+))</SCORprocess_name>"
      "(?i)<RawMACAddress>({src_mac}.+?)</RawMACAddress>"
      "(?i)<MachineName>({src_host}.+?)</MachineName>"
      "(?i)<SCORevent_name>({action}.+?)</SCORevent_name>"
      "(?i)<IPAddress>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?</IPAddress>"
      "(?i)<OSName>({os}.+?)</OSName>"
    ]
  

}
```