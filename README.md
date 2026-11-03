# pg_bigm — Windows x64

[日本語](README_ja.md) | English

pgextwin provides **unofficial Windows x64 binaries** of [pg_bigm](https://github.com/pgbigm/pg_bigm). pg_bigm adds bigram-based text search to PostgreSQL.

## Download and compatibility

Download the ZIP for your PostgreSQL major from the [latest published Release](https://github.com/pgextwin/pg_bigm/releases/latest) or [all Releases](https://github.com/pgextwin/pg_bigm/releases). Published PostgreSQL **14–18** packages are listed in the [pgextwin catalog](https://pgextwin.github.io/website/en/). PostgreSQL 14 community support ends November 12, 2026. Older files may remain available.

## Installation

1. Back up your installation and review [upstream pg_bigm documentation](https://github.com/pgbigm/pg_bigm).
2. Stop PostgreSQL before replacing files. Extract the ZIP matching your PostgreSQL major and copy the included lib/ and share/extension/ contents to the corresponding PostgreSQL directories.
3. Load pg_bigm with shared_preload_libraries or session_preload_libraries as appropriate for your use case; changing shared preload requires a server restart. Start PostgreSQL after installing the package.
4. Run CREATE EXTENSION pg_bigm; in each database that needs the extension.

More detailed Windows installation notes: [docs/windows_ja.md](docs/windows_ja.md).

Check SHA256SUMS.txt attached to the Release against your downloaded ZIP. Consult the Release for any SPDX SBOM, vulnerability report and signed attestations. Test before production deployment.

## License

The upstream project documents functionality, settings and limitations. This is an independent, unofficial Windows package; see the license notices included in the distribution.
