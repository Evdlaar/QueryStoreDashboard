# Query Store Dashboards
[![licence badge]][licence]
[![stars badge]][stars]
[![forks badge]][forks]
[![issues badge]][issues]

[licence badge]:https://img.shields.io/badge/license-MIT-blue.svg
[stars badge]:https://img.shields.io/github/stars/Evdlaar/QueryStoreDashboard.svg
[forks badge]:https://img.shields.io/github/forks/Evdlaar/QueryStoreDashboard.svg
[issues badge]:https://img.shields.io/github/issues/Evdlaar/QueryStoreDashboard.svg

[licence]:https://github.com/Evdlaar/QueryStoreDashboard/blob/master/LICENSE.md
[stars]:https://github.com/Evdlaar/QueryStoreDashboard/stargazers
[forks]:https://github.com/Evdlaar/QueryStoreDashboard/network
[issues]:https://github.com/Evdlaar/QueryStoreDashboard/issues

The Query Store Dashboards provides additional query performance information on databases that have the Query Store feature enabled and can be loaded by adding the **.rdl** file as a custom report in SQL Server Management Studio.

You can download the **.rdl** files by selecting the **.zip** file and select the option "Download".
Alternatively you can select the “Release” button and download the “QueryStoreDashboards” .zip file that contains all the Query Store Dashboards.

Installation and usage information can be found on the Wiki.

The dashboard requires Microsoft SQL Server 2016 and Microsoft SQL Server Management Studio 2016 to work.

## Release notes

### Query Store Database Dashboard v1.3


- Forced execution plan overview removed
  Instead you should use sp_WhatsupQueryStore to quickly analyse forced plans by running
  EXEC sp_WhatsupQueryStore @dbname = 'your database', @return_forced_plans = 1.

  You can download sp_WhatsupQueryStore through GitHub at https://github.com/Evdlaar/sp_WhatsupQueryStore.

- Added Queries with multiple plans performance chart.
  This chart, unlike the other ones, uses a logarithmic scale to improve readability when query duration between plans have large difference between durations.

- Removed unused datasets.

- Changed date/time format on x-axis in charts to exclude the date and only show time.

- Modified queries to avoid potential locking situations.


The Query Store Dashboards are developed and maintained by Enrico van de Laar (@evdlaar).


## License
[MIT](/LICENSE.md)
