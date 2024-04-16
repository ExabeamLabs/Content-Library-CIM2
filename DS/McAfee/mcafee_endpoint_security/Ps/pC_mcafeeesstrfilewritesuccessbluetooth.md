#### Parser Content
```Java
{
Name = mcafee-es-str-file-write-success-bluetooth
  ParserVersion = "v1.0.0"
  Vendor = McAfee
  Product = McAfee Endpoint Security
  TimeFormat = ["yyyy-MM-dd HH:mm:ss","epoch_sec"]
  Conditions = [ """|Bluetooth""", """|10000|""" ]
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
      """^([^|]*\|){20}(({domain}[^\\]+?)\\)?({user}[\w\.\-]{1,40}\$?)\|""",
      """\|({time}\d+)\.\d+\s*$""",
      ]


}
```