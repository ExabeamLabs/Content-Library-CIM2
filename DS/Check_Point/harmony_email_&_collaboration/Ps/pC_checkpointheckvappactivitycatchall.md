#### Parser Content
```Java
{
Name = "checkpoint-hec-kv-app-activity-catchall"
 Vendor = "Check Point"
 Product = "Harmony Email & Collaboration"
 TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSZ" ]
 ParserVersion = v1.0.0
 Conditions = [ """","module":"""", """","category":"""", ""","eventData":"""", """","event":"""", """","severity":""""]
 Fields  = [
  """"severity":"({severity}[^"]+)""""
  """"module":"({product_name}[^"]+)""""
  """"event":"({event_name}({operation}[^"]+))""""
  """"eventData":"({additional_info}[^"]+)""""
  """"eventData":"Login succeed for client with IP:\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"createdBy":"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
  """"authType":"({auth_type}[^"]+)""""
  """"category:"({category}[^"]+)""""
  """"_tenant_id:"({tenant_id}[^"]+)""""
  """"createdAt":"({time}\d{4}-\d{2}-\d{2}T(\d{2}:){2}\d{2}\.\d+Z)""""
 ]


}
```