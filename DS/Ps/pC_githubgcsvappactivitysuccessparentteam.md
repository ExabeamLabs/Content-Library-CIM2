#### Parser Content
```Java
{
Name = "github-g-csv-app-activity-success-parentteam"
Conditions = [
  """team.change_parent_team,"""
]
ParserVersion = "v1.0.0"

json-github-actions-1.Fields} [
      """exa_json_path=$..host,exa_field_name=host"""
      """exa_json_path=$..audit.action,exa_field_name=operation"""
      """exa_json_path=$..audit.actor_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
      """exa_json_path=$..audit.user,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  
}
```