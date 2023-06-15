#### Parser Content
```Java
{
Name = airlock-sah-json-network-traffic-connectiontrace
  ParserVersion = v1.0.0
  Vendor = Airlock
  Product = Airlock Security Access Hub
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"sess_id":"""", """"rcpt_id":"""", """"program":"""" ]
  Fields = [
    """({time}\d+\-\d+\-\d+T\d+:\d+:\d+)\.\d+[\+\-]\d+:\d+\s+({host}[\w\-.]+)\s+\{""",
    """"sess_id":"({session_id}[^"]+)""",
# req_id is removed
# rcpt_id is removed
# program is removed
    """"priority":"({priority}[^"]+)""",
    """"pid":"({process_id}[^"]+)""",
    """"message":"({event_name}.+?)","""",
# mapping is removed
    """"log_id":"({event_id}[^"]+)""",
# log_cat is removed
    """"host":"({host}[^"]+)""",
# facility is removed
    """"client_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
# audit_token is removed
  ]


}
```