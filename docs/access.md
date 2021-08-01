# Connection Name

.NET Libraries | OLE DB Providers | ODBC Drivers | Wrappers and others
--- | --- | --- | ---
&nbsp; | [Microsoft ACE OLEDB 12.0](#microsoft-ace-oledb-12.0) | [Microsoft Access accdb ODBC Driver](#microsoft-access-accdb-odbc-driver) | [.NET Framework Data Provider for OLE DB](#.net-framework-data-provider-for-ole-db)
&nbsp; | [Microsoft Jet OLE DB 4.0](#microsoft-ace-ole-db-4.0) | [Microsoft Access ODBC Driver](#microsoft-access-odbc-driver) | [.NET Framework Data Provider for ODBC](#.net-framework-data-provider-for-odbc)

----

## Microsoft ACE OLEDB 12.0
### Standard security
```
Provider=Microsoft.ACE.OLEDB.12.0;Data Source=C:\myFolder\myAccessFile.accdb;Persist Security Info=False;
```

Access 2007
Access 2010
Access 2013

### With database password
This is the connection string to use when you have an Access 2007 - 2013 database protected with a password using the "Set Database Password" function in Access.

```
Provider=Microsoft.ACE.OLEDB.12.0;Data Source=C:\myFolder\myAccessFile.accdb;Jet OLEDB:Database Password=MyDbPassword;
```

Some reports of problems with password longer than 14 characters. Also that some characters might cause trouble. If you are having problems, try change password to a short one with normal characters.

**Note!** Reports say that a database encrypted using Access 2010 - 2013 default encryption scheme does not work with this connection string. In Access; try options and choose 2007 encryption method instead. That should make it work. We do not know of any other solution. Please get in touch if other solutions is available!

Access 2007
Access 2010
Access 2013

### DataDirectory functionality
```
Provider=Microsoft.ACE.OLEDB.12.0;Data Source=|DataDirectory|\myAccessFile.accdb;Persist Security Info=False;
```

Access 2007
Access 2010
Access 2013

### Network Location
``` 
Provider=Microsoft.ACE.OLEDB.12.0;Data Source=\\server\share\folder\myAccessFile.accdb;
```
Access 2007
Access 2010
Access 2013

### Standard security (mdb file)
```
Provider=Microsoft.ACE.OLEDB.12.0;Data Source=C:\myFolder\myAccessFile.mdb;Persist Security Info=False;
```

Access 97
Access 2000
Access 2002
Access 2003

### With database password (mdb file)
This is the connection string to use when you have an Access 97 - 2003 database protected with a password using the "Set Database Password" function in Access.

```
Provider=Microsoft.ACE.OLEDB.12.0;Data Source=C:\myFolder\myAccessFile.mdb;Jet OLEDB:Database Password=MyDbPassword;
```

Some reports of problems with password longer than 14 characters. Also that some characters might cause trouble. If you are having problems, try change password to a short one with normal characters.

Access 97
Access 2000
Access 2002
Access 2003

### DataDirectory functionality (mdb file)
```
Provider=Microsoft.ACE.OLEDB.12.0;Data Source=|DataDirectory|\myAccessFile.mdb;Persist Security Info=False;
```

Access 97
Access 2000
Access 2002
Access 2003

### Network Location (mdb file)
```
Provider=Microsoft.ACE.OLEDB.12.0;Data Source=\\serverName\shareName\folder\myAccessFile.mdb;
```

Access 97
Access 2000
Access 2002
Access 2003

----
## Microsoft Jet OLE DB 4.0
### Standard security
```
Provider=Microsoft.Jet.OLEDB.4.0;Data Source=C:\mydatabase.mdb;User Id=admin;Password=;
```
[How to Use JET in 64 bit environments - TODO - add link](TODO-add-link)

Access 97
Access 2000
Access 2002
Access 2003

### With database password
This is the connection string to use when you have an access database protected with a password using the Set Database Password function in Access.

```
Provider=Microsoft.Jet.OLEDB.4.0;Data Source=C:\mydatabase.mdb;Jet OLEDB:Database Password=MyDbPassword;
```

Some reports of problems with password longer than 14 characters. Also that some characters might cause trouble. If you are having problems, try change password to a short one with normal characters.

Access 97
Access 2000
Access 2002
Access 2003

### Workgroup (system database)
```
Provider=Microsoft.Jet.OLEDB.4.0;Data Source=C:\mydatabase.mdb;Jet OLEDB:System Database=system.mdw;
```

Access 97
Access 2000
Access 2002
Access 2003

### Workgroup (system database) specifying username and password
```
Provider=Microsoft.Jet.OLEDB.4.0;Data Source=C:\mydatabase.mdb;Jet OLEDB:System Database=system.mdw;User ID=myUsername;Password=myPassword;
```

Access 97
Access 2000
Access 2002
Access 2003

### DataDirectory functionality
```
Provider=Microsoft.Jet.OLEDB.4.0;Data Source=|DataDirectory|\myDatabase.mdb;User Id=admin;Password=;
```

Access 97
Access 2000
Access 2002
Access 2003

### Network Location
```
Provider=Microsoft.Jet.OLEDB.4.0;Data Source=\\serverName\shareName\folder\myDatabase.mdb;User Id=admin;Password=;
```

Access 97
Access 2000
Access 2002
Access 2003

### Using RDS (MS Remote)
Access database over HTTP. You must setup RDS on the server for his to work.
```
Provider=MS Remote;Remote Provider=Microsoft.Jet.OLEDB.4.0;Remote Server=http://server.adress.com;Data Source=d:\myPath\myDatabase.mdf;
```

Access 97
Access 2000
Access 2002
Access 2003

### Exclusive
Used to get exclusive access to the database if you, for instance, want to let the application be able to reset the database password.
```
Provider=Microsoft.Jet.OLEDB.4.0;Data Source=C:\mydatabase.mdb;Mode=Share Exclusive;User Id=admin;Password=;
```

Access 97
Access 2000
Access 2002
Access 2003

----
## .NET Framework Data Provider for OLE DB
### Use an OLE DB provider from .NET
```
Provider=any oledb provider's name;OledbKey1=someValue;OledbKey2=someValue;
```

See the respective OLEDB provider's connection strings options. The .net OleDbConnection will just pass on the connection string to the specified OLEDB provider. Read more here.

----
## Microsoft Access accdb ODBC Driver
### Standard Security
```
Driver={Microsoft Access Driver (*.mdb, *.accdb)};Dbq=C:\mydatabase.accdb;Uid=Admin;Pwd=;
```

Access 2007
Access 2010
Access 2013

### Workgroup
```
Driver={Microsoft Access Driver (*.mdb, *.accdb)};Dbq=C:\mydatabase.accdb;SystemDB=C:\mydatabase.mdw;
```

No changes were made to the .mdw file format for Office Access 2007. The Office Access 2007 Workgroup Manager creates .mdw files that are identical to those that are created in Access 2000 through Access 2003. The .mdw files that are created in those earlier versions can be used by databases in Office Access 2007.

Access 2007
Access 2010
Access 2013

### Exclusive
```
Driver={Microsoft Access Driver (*.mdb, *.accdb)};Dbq=C:\mydatabase.accdb;Exclusive=1;Uid=admin;Pwd=;
```

Access 2007
Access 2010
Access 2013

### Enable admin statements
To enable certain programatically admin functions such as CREATE USER, CREATE GROUP, ADD USER, GRANT, REVOKE and DEFAULTS (when making CREATE TABLE statements) use this connection string.
```
Driver={Microsoft Access Driver (*.mdb, *.accdb)};Dbq=C:\mydatabase.accdb;Uid=Admin;Pwd=;ExtendedAnsiSQL=1;
```

Access 2007
Access 2010
Access 2013

### Specifying locale identifier
Use this one to specify the locale identifier which can help with non-US formated dates.
```
Driver={Microsoft Access Driver (*.mdb, *.accdb)};Dbq=C:\mydatabase.accdb;Locale Identifier=2057;Uid=Admin;Pwd=;
```

The above example uses the en-gb locale identifier (2057)

Access 2007
Access 2010
Access 2013

### Standard connection
```
Driver={Microsoft Access Driver (*.mdb, *.accdb)};Dbq=C:\mydatabase.mdb;
```

Access 97
Access 2000
Access 2002
Access 2003

----
## Microsoft Access ODBC Driver
### Standard Security
```
Driver={Microsoft Access Driver (*.mdb)};Dbq=C:\mydatabase.mdb;Uid=Admin;Pwd=;
```

Access 97
Access 2000
Access 2002
Access 2003

### Workgroup
```
Driver={Microsoft Access Driver (*.mdb)};Dbq=C:\mydatabase.mdb;SystemDB=C:\mydatabase.mdw;
```

Access 97
Access 2000
Access 2002
Access 2003

### Exclusive
```
Driver={Microsoft Access Driver (*.mdb)};Dbq=C:\mydatabase.mdb;Exclusive=1;Uid=admin;Pwd=;
```

Access 97
Access 2000
Access 2002
Access 2003

### Enable admin statements
To enable certain programatically admin functions such as CREATE USER, CREATE GROUP, ADD USER, GRANT, REVOKE and DEFAULTS (when making CREATE TABLE statements) use this connection string.
```
Driver={Microsoft Access Driver (*.mdb)};Dbq=C:\mydatabase.mdb;Uid=Admin;Pwd=;ExtendedAnsiSQL=1;
```

Access 97
Access 2000
Access 2002
Access 2003

### Specifying locale identifier
Use this one to specify the locale identifier which can help with non-US formated dates.
```
Driver={Microsoft Access Driver (*.mdb)};Dbq=C:\mydatabase.mdb;Locale Identifier=2057;Uid=Admin;Pwd=;
```

The above example uses the en-gb locale identifier (2057)

Access 97
Access 2000
Access 2002
Access 2003

----
## .NET Framework Data Provider for ODBC
### Use an ODBC driver from .NET
```
Driver={any odbc driver's name};OdbcKey1=someValue;OdbcKey2=someValue;
```

See the respective ODBC driver's connection strings options. The .net OdbcConnection will just pass on the connection string to the specified ODBC driver. Read more here.
