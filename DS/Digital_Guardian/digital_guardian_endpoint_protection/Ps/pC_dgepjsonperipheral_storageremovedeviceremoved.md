#### Parser Content
```Java
{
Name = dg-ep-json-peripheral_storage-remove-deviceremoved
  Vendor = Digital Guardian
  Product = Digital Guardian Endpoint Protection
  TimeFormat = "epoch"
  Conditions = [ """"_time":""", """"Event Display Name":"""", """"Device Removed"""" ]
  Fields = [
    """"_time":({time}\d{13})""",
    """"Computer Name":"([^\\\/]+?[\\\/]+)?({host}[^"]+)""",
    """"User":"({user}[^"]+)""",
    """"Process Domain":"({web_domain}[^"]+)""",
    """"Process PID":({process_id}\d+)""",
    """"Application":"({app}[^"]+)""",
    """"MD5 Hash":"({hash_md5}[^"]+)""",
    """"SHA1 Hash":"({hash_sha1}[^"]+)""",
    """"Event Display Name":"({operation}[^"]+)""",
    """"Process Path":"({process_path}({process_dir}[^"]+(\\|\/)+)?({process_name}[^"]+))"""",
  ]
  ParserVersion = "v1.0.0"


}
```