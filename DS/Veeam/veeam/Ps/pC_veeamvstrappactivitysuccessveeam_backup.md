#### Parser Content
```Java
{
Name = "veeam-v-str-app-activity-success-veeam_backup"
    Vendor = "Veeam"
    Product = "Veeam"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
    Conditions = [ """Veeam_Backup""", """[origin""" ]
    Fields = [
      """({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d[+-]\d\d:\d\d) ({host}[\w.-]+) ({app}Veeam_Backup)(\s+\S+){2}\s+\[({additional_info}[^\]]+)\]\s+({event_name}.+?)$"""       
    ]
    ParserVersion = "v1.0.0"


}
```