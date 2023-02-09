#### Parser Content
```Java
{
Name = beyondtrust-privmgmt-kv-process-create-success-processstarted
    Vendor = BeyondTrust
    Product = BeyondTrust Privilege Management
    TimeFormat = "MM/dd/yyyy HH:mm:ss a"
    Conditions = [ """SourceName =Avecto Defendpoint Service""", """Message=Process started"""]
    Fields = [
      """ComputerName =({host}[^\s]+)""",
      """Message=({operation_type}.+?)\s+Command Line:""",
      """User Name:\s*(?:[A-F\d\-]{36}|({user}.+?))\s+User Domain SID:""",
      """User Domain Name:\s*({domain}.*?)\s+User Domain Name""",
      """User SID:\s*({user_sid}.*?)\s+User Name""",
      """Token:\s*({token}.*?)\s+Token Description:""",
      """MD5:\s*({hash_md5}[^\s]+)""",
      """Command Line:\s*({process_command_line}.+?)\s*Process Id:""",
      """Message Description:\s*(<.+?>)?\s+(Unique Process ID:)?\s*({process_guid}[^\s]+)\s+Workstyle ID:""",
      """Parent Process Unique ID:\s*(?:<None>|({parent_process_guid}[^\s]+))\s+Parent Process File Name:""",
      """File Name:\s*({process_path}({process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({process_name}.+?))\s+Hash:"""
      """Parent Process File Name:\s*({parent_process}({parent_process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({parent_process_name}.+?))\s+COM CLSID:"""
    ]
  DupFields = [ "host->dest_host","process_guid->process_id" ]
  ParserVersion = "v1.0.0"
  

}
```