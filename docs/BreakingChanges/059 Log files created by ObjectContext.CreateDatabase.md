## 59: Log files created by the ObjectContext.CreateDatabase method

### Scope
Edge

### Version Introduced
4.5

### Source Analyzer Status
Planned

### Change Description
When the CreateDatabase method is called either directly or by using Code First with the SqlClient provider and an AttachDBFilename value in the connection string, it creates a log file named filename_log.ldf instead of filename.ldf (where filename is the name of the file specified by the AttachDBFilename value). This change improves debugging by providing a log file named according to SQL Server specifications.

- [ ] Quirked
- [ ] Build-time break

### Recommended Action
If the log file name is important for an app, the app should be updated to expect the standard _log.ldf file name format.

### Affected APIs
* `M:System.Data.Objects.ObjectContext.CreateDatabase`

[More information](https://msdn.microsoft.com/en-us/library/hh367887(v=vs.110).aspx#sql)