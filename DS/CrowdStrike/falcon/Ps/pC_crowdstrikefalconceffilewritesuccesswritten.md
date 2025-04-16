#### Parser Content
```Java
{
Name = "crowdstrike-falcon-cef-file-write-success-written"
    ParserVersion = "v1.0.0"
    Conditions = [
""""event_simpleName":"""
"""Written""""
]
Fields = ${CrowdStrikeParsersTemplates.crowdstrike-file-operations.Fields} [
""""(ImageFileName|TargetFileName)":\s*"({file_path}({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+?(\.(\d+|({file_ext}\w{1,10}?)))?))\s*"""",
"""exa_regex="(ImageFileName|TargetFileName)":\s*"({file_path}({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+?(\.(\d+|({file_ext}\w{1,10}?)))?))\s*""""
]
  
crowdstrike-file-operations = {
Vendor = "CrowdStrike"
Product = "Falcon"
ExtractionType = json
TimeFormat = ["epoch","epoch_sec"]
Fields = [
""""timestamp":\s*"({time}\d{10,13})"""
""""event_simpleName":\s*"({event_code}[^"]+)"""
""""aid":\s*"({aid}[^"]+)"""
""""SourceFileName":\s*"({src_file_dir}[^"]+\\+)?({src_file_name}[^\\"]+)"""
"""suser=(system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""src-account-name":"({account_name}[^"]+)"""
""""((?i)SHA256String|SHA256HashData)":"({hash_sha256}[^"]+)""""
""""name":"({event_name}[^"]+)""""
""""UserName":"(({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
""""ContextProcessId":"({process_guid}[^"]+)""""
""""aip":"({aip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""Size":"({bytes}\d+)"""",
""""cid":"({cid}[^"]+)""",
""""event_platform":\s*"({os}[^"]+)"""",
""""OciContainerId"\s*:\s*"({container_id}[^"]+)"""",
""""ShareAccess":"({access}[^"]+)""""
""""FileObject":"({object}[^"]+)""""
""""FileAttributes":"({attributes}[^"]+)""""
""""(ImageFileName|TargetFileName)":\s*"({file_path}[^"]+)""",
""""(ImageFileName|TargetFileName)":\s*"({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+?(\.(\d+|({file_ext}\w{1,10}?)))?)\s*"""",
""""ContextBaseFileName":"({file_name}[^"]+)"""",
"""exa_json_path=$.timestamp,exa_field_name=time""",
"""exa_json_path=$.event_simpleName,exa_field_name=event_code""",
"""exa_json_path=$.aid,exa_field_name=aid""",
"""exa_json_path=$.SourceFileName,exa_regex=^({src_file_path}({src_file_dir}[^"]*[\\\/]+)({src_file_name}[^\\\/"]+?(\.(\d+|({src_file_ext}[^\\\/"\-\.\_]{1,10}?)))?))$"""
"""exa_json_path=$.TargetFileName,exa_field_name=file_path""",
"""exa_regex="TargetFileName":\s*"({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+?(\.(\d+|({file_ext}[^\\\/"\-\.\_\$]{1,10}?)))?)\s*""""
"""exa_regex="((?i)SHA256String|SHA256HashData)":"({hash_sha256}[^\"]+)""""
"""exa_json_path=$.name,exa_field_name=event_name""",
"""exa_json_path=$.UserName,exa_regex=(({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
"""exa_json_path=$.ContextProcessId,exa_field_name=process_guid""",
"""exa_json_path=$.aip,exa_regex=({aip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
"""exa_json_path=$.Size,exa_field_name=bytes"""
"""exa_json_path=$.cid,exa_field_name=cid"""
"""exa_json_path=$.event_platform,exa_field_name=os""",
"""exa_json_path=$.OciContainerId,exa_field_name=container_id"""
"""exa_json_path=$.ShareAccess,exa_field_name=access"""
"""exa_json_path=$.FileObject,exa_field_name=object"""
"""exa_json_path=$.FileAttributes,exa_field_name=attributes"""
"""exa_regex="(ImageFileName|TargetFileName)":\s*"({file_path}[^"]+)""",
"""exa_regex="(ImageFileName|TargetFileName)":\s*"({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+?(\.(\d+|({file_ext}\w{1,10}?)))?)\s*""""
"""exa_json_path=$.ContextBaseFileName,exa_field_name=file_name"""

}
```