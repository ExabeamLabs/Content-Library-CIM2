#### Parser Content
```Java
{
Name = mcafee-es-file-write-success-bluetooth
  ParserVersion = "v1.0.0"
  Vendor = McAfee
  Product = McAfee Endpoint Security
  TimeFormat = "epoch_sec"
  Conditions = [ """|Bluetooth""" ]
  Fields = [
      """^.*?({alert_id}\d+)\|""",
      """^([^|]*\|){11}({device_type}[^|]+)\|""",
      """^([^|]*\|){14}({dest_ip}[a-fA-F0-9.:]+)\|""",
      """^([^|]*\|){15}({dest_host}[^|]+)\|""",
      """^([^|]*\|){17}({file_name}[^|]+)""",
      """^([^|]*\|){19}({file_path}[^|]+)""",
      """^([^|]*\|){19}({file_path}[^|]*?({file_name}[^\\\/|]+))\|""",
      """^([^|]*\|){16}({file_path}[^|]+)""",
      """^([^|]*\|){16}({file_path}[^|]*?({file_name}[^\\\/|]+))\|""",
      """^([^|]*\|){20}(({domain}[^\\]+?)\\)?({user}[^|\\]+)\|""",
      """\|({time}\d+\.\d+)\s*$""",
      ]


}
```