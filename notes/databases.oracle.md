---
id: tn0a5nqbrce9yebvej9h736
title: Oracle
desc: ''
updated: 1677667276305
created: 1677666402987
---

### Export a database dump  
```shell
exp <user>/<password>@<pluggableDB>
```
- buffer size: 4096 >
- export file: EXPDAT>DMP > myDump.dmp
- (1) Entire database (2) Users, or (3)Tables : (2)Users >
- Export grants (yes/no): yes >
- Export table data (yes/no): yes >
- Compress extents (yes/no): yes >
- Export done in WE8MSWIM1252 character set...
- User to be exported: (RETURN to quit) > schema_user
- exporting...
