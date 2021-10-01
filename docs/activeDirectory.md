# Active Directory connection strings
.NET Libraries | OLE DB Providers | ODBC Drivers | Wrappers and others
--- | --- | --- | ---
&nbsp; | [Active Directory OLE DB provider](#active-directory-ole-db-provider) | &nbsp; | [].NET Framework Data Provider for OLE DB](#net-framework-data-provider-for-odbc)


## Active Directory OLE DB provider
### Standard
```
    Provider=ADSDSOObject;
```

### Specifying user name and password
```
    Provider=ADSDSOObject;User Id=myUsername;Password=myPassword;
```

## .NET Framework Data Provider for OLE DB
### Use an OLE DB provider from .NET
```
    Provider=any oledb provider's name;OledbKey1=someValue;OledbKey2=someValue;
```

    See the respective OLEDB provider's connection strings options. The .net OleDbConnection will just pass on the connection string to the specified OLEDB provider. 