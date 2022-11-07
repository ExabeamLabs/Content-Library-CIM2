#### Parser Content
```Java
{
Name = code42-incydr-csv-file-delete-success-code42logcollector
  Vendor = Code42
  Product = Code42 Incydr
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ParserVersion = "v1.0.0"
  Conditions= [ """KAFKA_CONNECT_SYSLOG: Code42LogCollector,""""]
  Fields = [
    """KAFKA_CONNECT_SYSLOG: Code42LogCollector,.*?,.*?,(|({access}[^,]+)),({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ),.*?,(|({file_path}[^,]+)),(|({file_name}[^,]+)),(|({file_type}[^,]+)),(|({file_category}[^,]+)),(|({bytes}\d+)),(|({file_owner}[^,]+)),(|({md5}[^,]+)),(|({sha256}[^,]+)),(|({time_created}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)),(|({time_modified}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)),(|({email_address}[^,]+)),(|({device_id}[^,]+)),(|({user_uid}[^,]+)),(|({host}[^,]+)),(|({domain}[^,]+)),(|({src_ip}[^,]+)),(|({private_ip}[^,]+)),(|({actor}[^,]+)),(|({process_dir}[^,]+)),(|({log_source}[^,]+)),(|({url}[^,]+)),(|({shared}[^,]+)),(|({shared_with}[^,]+)|"({=shared_with}[^"]+))",(|({file_exposure_changed_to}[^,]+)),(|({cloud_drive_id}[^,]+)),(|({detection_source_alias}[^,]+)),(|({file_id}[^,]+)),(|({exposure_type}[^,]+)),(|({process_owner}[^,]+)),(|({process_path}[^,]+)),(|({tab_title}[^,]+)),,(|({tab_url}[^,]+)),(|({removable_media_vendor}[^,]+)),(|({removable_media_name}[^,]+)),(|({removable_media_serial_number}[^,]+)),(|({removable_media_capacity}[^,]+)),(|({removable_media_bus_type}[^,]+)),(|({removable_media_media_name}[^,]+)),(|({removable_media_volume_name}[^,]+)),(|({removable_media_partition_id}[^,]+)),(|({sync_destination}[^,]+)),(|({email_dlp_policy_names}[^,]+)),(|({email_subject}[^,]+)),(|({sender}[^,]+)),(|({email_dlp_from}[^,]+))"""
]
  DupFields = ["file_path->file_dir"]


}
```