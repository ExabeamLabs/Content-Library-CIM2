#### Parser Content
```Java
{
Name = tanium-tr-json-database-activity-inteldb
 ParserVersion = v1.0.0
 Product = Tanium Threat Response
 Conditions = [ """"table":"IntelDb"""", """"action":"""", """"rowId":""", """"revision":""", """"state":""" ]
 Vendor = Tanium
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
 Fields=[
    """"createdAt":"({time}[^"]+)"""",
    """"type":"({alert_type}[^"]+)"""",
    """"connId":"({connection_id}[^"]+)"""",
    """"directoryPath":"({process_dir}[^"]+)"""",
    """"userName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """"action":"({action}[^"]+)"""",
    """"dst":"(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))|({dest_host}[^"]+))"""",
# ids is removed
    """"path":"({file_path}({file_dir}.*?)({file_name}[^\\\/;"]+?(\.({file_ext}[^\.;\\"]+?))?))"""",
    """"name":"({alert_name}[^"]+)"""",
# dest_type is removed
    """"query":"({query}.+?)",""",
    """"userId":({user_id}\d+)""",
    """"revision":(null|({revision}\d+))""",
# is_delta is removed
# is_sync is removed
# intel_mapping is removed
  ]


}
```