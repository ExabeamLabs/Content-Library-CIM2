#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-file-download-success-bitsjobcreated
    ParserVersion = "v1.0.0"
    TimeFormat = "epoch"
    Conditions = [
""""event_simpleName":"BITSJobCreated""""
]
Fields = ${CrowdStrikeParsersTemplates.crowdstrike-file-operations.Fields}[
    """"timestamp":\s*"*({time}\d{13})""""
   ]
  
crowdstrike-file-operations = {
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch_sec"
Fields = [
""""timestamp":\s*"({time}\d{10})"""
""""event_simpleName":\s*"({event_code}[^"]+)"""
""""aid":\s*"({aid}[^"]+)"""
""""SourceFileName":\s*"({src_file_dir}[^"]+\\+)?({src_file_name}[^\\"]+)"""
""""TargetFileName":\s*"({file_path}[^"]+)"""
""""TargetFileName":\s*"({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+?(\.(\d+|({file_ext}[^\\\/"\-\.\_]{1,10}?)))?)\s*""""
"""suser=(system|({user}[^\s]+))"""
"""src-account-name":"({account_name}[^"]+)"""
""""((?i)SHA256String|SHA256HashData)":"({hash_sha256}[^"]+)""""
""""name":"({event_name}[^"]+)""""
""""UserName":"(({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))""""
""""ContextProcessId":"({process_guid}[^"]+)""""
""""aip":"({aip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""Size":"({bytes}\d+)""""

}
```