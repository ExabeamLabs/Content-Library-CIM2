#### Parser Content
```Java
{
Name = mcafee-nsm-csv-app-login-fail-failed
  ParserVersion = "v1.0.0"
  Conditions = [ """Network Security Manager Login; failed;""", """; User;""" ]

mcafee-nsm-app-events = {
    Vendor = McAfee
    Product = McAfee NSM
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd HH:mm:ss z"
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d\s\w+);""",
      """({app}Network Security Manager)""",
      """User\s+"+(Administrator|({full_name}[^"]+))""",
      """;\s+({user}\w+); User;""",
      """login\s(ID|id|Id)\s+"+({user}[^"]+)""",
      """from\s+"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """protocol\s+:\s+(null|({protocol}[^.\/;]+))""",
      """Login URI:\s*(null|({uri_path}.+?))\s*,\s*URI""",
      """({result}succeeded|failed);""",
      """({event_name}Network Security Manager Login; (succeeded|failed));""",
    
}
```