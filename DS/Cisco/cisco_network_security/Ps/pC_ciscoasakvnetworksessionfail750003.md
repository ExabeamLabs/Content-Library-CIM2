#### Parser Content
```Java
{
Name = cisco-asa-kv-network-session-fail-750003
  Vendor = Cisco
  Product = Cisco Network Security
  ParserVersion = v1.0.0
  TimeFormat = ["MMM dd yyyy HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ """-750003""", """Negotiation aborted due to ERROR""" ]
  Fields = [
    """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
"""\s(({host}[\w.\-]+))\s+([-\s:]+)?%ASA""",
    """(({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s*)?({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)""",
    """%ASA\-({priority}\d+)\-({event_code}\d+)""",
    """Local:(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?)):({dest_port}\d+)""",
    """Remote:(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?)):({src_port}\d+)""",
    """Username:({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+({protocol}\w+)?\s*({event_name}Negotiation aborted due to ERROR)""",
    """ERROR:\s*(|({result_reason}.*?))\s*$"""
  ]
  DupFields = [ "result_reason->failure_reason" ]


}
```