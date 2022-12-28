#### Parser Content
```Java
{
Name = zeek-z-str-file-read-success-fileslog
  ParserVersion = v1.0.0
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "epoch_sec"
  Conditions = [ """/files.log""" ]
  Fields = [
      """({time}\d{10})\.\d{6}\s+({file_id}[^\s]+)\s+(?:-|(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+))\s+(?:-|(({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+))\s+(?:-|({connection_uid}[^\s]+))\s+(?:-|({protocol}[^\s]+))\s+(?:-|({depth}[^\s]+))\s+(?:-|({analyzers}[^\s]+))\s+(?:-|({mime}[^\s]+))\s+(?:-|([^\s]+))\s+(?:-|({duration}[^\s]+))\s+(?:-|({local_orig}[^\s]+))\s+(?:-|({is_orig}[^\s]+))\s+(?:-|({bytes}\d+)?)\s+(?:-|({=bytes}\d+))\s+(?:-|({missed_bytes}\d*))\s+(?:-|({overflow_bytes}\d*))\s+(?:-|({timedout}[^\s]+))\s+(?:-|({parent_file_id}[^\s]+))\s+(?:-|({hash_md5}[^\s]+))\s+(?:-|({hash_sha1}[^\s]+))\s+(?:-|({hash_sha256}[^\s]+))\s+(?:-|({extracted}[^\s]+?))\s*""",
      """\d+\.\d{6}\s+([^\s]+\s+){22}(?:-|({extracted_cutoff}[^\s]+))\s+(?:-|({extracted_size}\d+))\s*"""
      """\d+\.\d{6}\s+([^\s]+\s+){8}(?:-|({file_path}({file_dir}[^\s]*?(\\u005c|[\\\/])*)({file_name}[^\s\\\/]+?(\.({file_ext}[^\s\\\/\.]+))?)))\s*\\?\s"""
  ]


}
```