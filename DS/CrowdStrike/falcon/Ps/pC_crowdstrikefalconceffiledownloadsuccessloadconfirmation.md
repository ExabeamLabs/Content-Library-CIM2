#### Parser Content
```Java
{
Name = crowdstrike-falcon-cef-file-download-success-loadconfirmation
    ParserVersion = "v1.0.0"
    TimeFormat = "epoch"
    Conditions = [
""""event_simpleName":"LFODownloadConfirmation""""
]
Fields = ${CrowdStrikeParsersTemplates.crowdstrike-file-operations.Fields}[
"""\"+aip\"+:\"+({aip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""DownloadPort\"+:\"+({dest_port}\d+)"""
"""DownloadServer\"+:\"+({dest_host}[^\"]+)"""
"""\"ConfigStateHash\":\"({old_hash}[^\"]+)"""
"""\"SHA256HashData\":\"({new_hash}[^\"]+)"""
""""timestamp":\s*"({time}\d{13})"""",
""""DownloadPath":"({file_url}({src_file_path}(({file_dir}[^"]+)[\\\/]+)?(({src_file_name}[^"\\\/]+?(\.({src_file_ext}[^\."]+))?))))"""",
""""TargetFileName":"({file_path}(({file_dir}[^"]+)[\\\/]+)?(({file_name}[^"\\\/]+?(\.({file_ext}[^\."]+))?)))""""
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
""""TargetFileName":\s*"({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+?(\.(\d+|({file_ext}[^\\\/"\-\.\_]+?)))?)\s*""""
"""suser=(system|({user}[^\s]+))"""
"""src-account-name":"({account_name}[^"]+)"""
""""((?i)SHA256String|SHA256HashData)":"({hash_sha256}[^"]+)""""
""""name":"({event_name}[^"]+)""""
"""UserName":"(({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|({user}[^"\s]+))""""
""""ContextProcessId":"({process_guid}[^"]+)""""
""""aip":"({aip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""Size":"({bytes}\d+)""""

}
```