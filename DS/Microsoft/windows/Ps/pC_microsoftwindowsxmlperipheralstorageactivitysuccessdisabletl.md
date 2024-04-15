#### Parser Content
```Java
{
Name = "microsoft-windows-xml-peripheral-storage-activity-success-disable-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Windows"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "a request was made to disable a device."
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime=\\'({time}\\d{4}-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d{9}Z)\\'\\/>"
      "(?i)<Computer>({dest_host}[^<>\"']+?)<\\/Computer>"
      "(?i)Security ID:\\s+({user_sid}[^\\s]+?)\\s+Account Name:"
      "(?i)Account Name:\\s+(-\\s*|({user}[^:]+?)\\s+)Account Domain:"
      "(?i)Device Name:\\s+({device_name}[^:]+?)\\s+Class ID:"
      "(?i)Device ID:\\s+({device_id}[^:]+?)\\s+Device Name:"
      "(?i)Account Domain:\\s+(-\\s*|({domain}[^:]+?)\\s+)Logon ID:"
      "(?i)Location Information:\\s+(|-|({additional_info}[^\\s]*?))(\\s+|\\s*\")"
      "(?i)Class Name:\\s+({device_type}[^:]+?)\\s+(Vendor IDs:|Hardware IDs:)"
      "(?i)({event_code}6419)"
      "(?i)>({event_code}6419)<\\/EventID>"
      "(?i)({event_name}A request was made to disable a device.)"
    ]
  

}
```