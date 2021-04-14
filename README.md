# PG Server GUI

GUI tool to run postgresql server in background, minimized to tray, without using the service, usefull if you want postgresql on external harddisk with data, maybe encrypted harddisk.

You need to add pgserver.ini next the exe file

pgpath: Path to exe bin folder of postgresql
datapath=Path to data, it should be initialized by

    initdb.exe -W -U postgres -D "d:\data\pg13" -E UTF8

tray: true if you want to make tray always show
minimized: start the application minimized
start: auto start server, work with minimzed too

Example of pgserver.ini

```
[options]
pgpath=d:\programs\pg13-64\bin
datapath=d:\data\pg13
tray=true
minimized=false
start=false
```

## Note

if you dont want to use this project, and want to install pg as server run this command once in admin privileges

    pg_ctl.exe register -N "pg13" -U "NT AUTHORITY\NetworkService" -D "d:\data\pg13" -w

## License

MIT(https://opensource.org/licenses/MIT)
