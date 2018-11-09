These two shell scripts can be used to deterministically get and set state from a postgres database.

First, the database gets dumped using pgdump.

Then, the real magic happens with the help of [Antti Kaihola's](https://github.com/akaihola) package, [split sort](https://github.com/akaihola/pgtricks/blob/master/pgtricks/pg_dump_splitsort.py). The data in the dump is split into new sql files by table name and sorted on the primary key.

Finally, a little cleanup.
