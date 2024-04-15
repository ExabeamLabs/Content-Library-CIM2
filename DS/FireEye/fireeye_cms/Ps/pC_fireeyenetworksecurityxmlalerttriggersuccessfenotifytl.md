#### Parser Content
```Java
{
Name = "fireeye-networksecurity-xml-alert-trigger-success-fenotify-tl"
    Vendor = "FireEye"
    Product = "FireEye CMS"
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [
      "fenotify-"
      "<src vlan="
    ]
    Fields = [
      "(?i)<occurred>({time}\\d\\d\\d\\d-\\d\\d-\\d\\d \\d\\d:\\d\\d:\\d\\d)"
      "(?i) fenotify-({alert_id}\\d+)"
      "(?i)<src vlan=\\\".+\\\">\\s*<ip>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?"
      "(?i)<src .+?<host>({src_host}[^<]+)"
      "(?i)<dst>.+?<ip>({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({dest_port}\\d+))?</ip"
    ]
    ParserVersion = "v1.0.0"
  

}
```