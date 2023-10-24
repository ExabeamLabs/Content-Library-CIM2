#### Parser Content
```Java
{
Name = code42-incydr-csv-file-delete-success-code42logcollector
  Vendor = Code42
  Product = Code42 Incydr
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.sssZ"
  time_createdFormat = ["yyyy-MM-dd HH:mm:ss"]
  time_modifiedFormat = ["yyyy-MM-dd HH:mm:ss"]
  ParserVersion = "v1.0.0"
  Conditions= [ """KAFKA_CONNECT_SYSLOG: Code42LogCollector,""""]
  Fields = [
    """KAFKA_CONNECT_SYSLOG: Code42LogCollector,.*?,.*?,(|({access}[^,]+)),({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ),.*?,(|({file_path}[^,]+)),(|({file_name}[^,]+)),(|({file_type}[^,]+)),(|({file_category}[^,]+)),(|({bytes}\d+)),(|({file_owner}[^,]+)),(|({hash_md5}[^,]+)),(|({sha256}[^,]+)),(|({time_created}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)),(|({time_modified}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)),(|({email_address}[^,]+)),(|({device_id}[^,]+)),(|({user_uid}[^,]+)),(|({host}[^,]+)),(|({domain}[^,]+)),(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?),(|({private_ip}[^,]+)),(|({actor}[^,]+)),(|({process_dir}[^,]+)),(|({log_source}[^,]+)),(|({url}[^,]+)),(|({shared}[^,]+)),(|({shared_with}[^,]+)|"({=shared_with}[^"]+))",(|({file_exposure_changed_to}[^,]+)),(|({cloud_drive_id}[^,]+)),(|({detection_source_alias}[^,]+)),(|({file_id}[^,]+)),(|({exposure_type}[^,]+)),(|({process_owner}[^,]+)),(|({process_path}[^,]+)),(|({tab_title}[^,]+)),,(|({tab_url}[^,]+)),(|({removable_media_vendor}[^,]+)),(|({removable_media_name}[^,]+)),(|({removable_media_serial_number}[^,]+)),(|({removable_media_capacity}[^,]+)),(|({removable_media_bus_type}[^,]+)),(|({removable_media_media_name}[^,]+)),(|({removable_media_volume_name}[^,]+)),(|({removable_media_partition_id}[^,]+)),(|({sync_destination}[^,]+)),(|({email_dlp_policy_names}[^,]+)),(|({email_subject}[^,]+)),(|({src_email_address}[^,]+)),(|({email_dlp_from}[^,]+))"""
]
  DupFields = ["file_path->file_dir"]


}
```