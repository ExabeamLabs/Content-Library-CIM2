# Code Changes for sentinelone-singularityp-cef-alert-trigger-success-newactivethreat (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'alert_name', 'alert_severity', 'alert_type', 'file_dir', 'file_ext', 'file_name', 'file_path', 'hash_md5', 'hash_sha1', 'hash_sha256', 'host', 'os_revision', 'process_name', 'process_path', 'src_domain', 'src_fqdn', 'src_host', 'src_host_type', 'src_interface', 'src_ip', 'src_mac', 'src_net_status', 'src_port', 'time', 'user'] |
| edit_regex_field | file_dir |  | ['\WfileName=({file_dir}[^\|]*?\\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)\\Desktop\\)?)({file_name}[^\\\|]+?({file_ext}[^\\\|\.]+)?)((\||\s+)\w+=|\s*$)', '\WfileName=({file_dir}[^\|]*?\\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)\\Desktop\\)?)({process_name}[^\\\|]+?({file_ext}[^\\\|\.]+)?)((\||\s+)\w+=|\s*$)'] |
| edit_regex_field | file_ext |  | ['\WfileName=({file_dir}[^\|]*?\\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)\\Desktop\\)?)({file_name}[^\\\|]+?({file_ext}[^\\\|\.]+)?)((\||\s+)\w+=|\s*$)', '\WfileName=({file_dir}[^\|]*?\\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)\\Desktop\\)?)({process_name}[^\\\|]+?({file_ext}[^\\\|\.]+)?)((\||\s+)\w+=|\s*$)'] |
| edit_regex_field | user |  | ['\WfileName=({file_dir}[^\|]*?\\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)\\Desktop\\)?)({file_name}[^\\\|]+?({file_ext}[^\\\|\.]+)?)((\||\s+)\w+=|\s*$)', '\WfileName=({file_dir}[^\|]*?\\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)\\Desktop\\)?)({process_name}[^\\\|]+?({file_ext}[^\\\|\.]+)?)((\||\s+)\w+=|\s*$)'] |
| added_regex_field | process_name |  | ['\WfileName=({file_dir}[^\|]*?\\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)\\Desktop\\)?)({process_name}[^\\\|]+?({file_ext}[^\\\|\.]+)?)((\||\s+)\w+=|\s*$)'] |
| added_regex_field | process_path |  | ['\WfilePath=(N/A|({process_path}[^\|]+?))((\||\s+)\w+=|\s*$)'] |
| removed_attribute | DupFields |  | N/A |