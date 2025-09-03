#### Parser Content
```Java
{
Name = "veeam-v-kv-app-activity-success-veeam_mp"
    Vendor = "Veeam"
    Product = "Veeam"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
    Conditions = [ """Veeam_MP""", """[origin""", """Description="""" ]
    Fields = [
      """({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d[+-]\d\d:\d\d) ({host}[\w.-]+) ({app}Veeam_MP)(\s+\S+){2}\s+\[({additional_info}[^\]]+)\]\s+"""      
      """categoryId=({category_id}\d+)"""
      """instanceId=({instance_id}\d+)"""
      """TaskSessionID="({session_id}[^"]+)""""
      """Status="({result}[^"]+)""""
      """JobDescription="({description}[^"]+)""""
      """SourceHostName ="({src_host}[^"]+)""""
      """Description="({event_name}[^"]+)""""
      """ActivityType="({category}[^"]+)""""
      """UserName ="(({domain}[^"\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
      """ObjectName ="({object}[^"]+)""""
    ]
    ParserVersion = "v1.0.0"


}
```