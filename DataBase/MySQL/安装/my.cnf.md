```
[client]
port = 3306
socket = /tmp/mysql.sock
default-character-set = utf8mb4

[mysqld]
skip-grant-tables=0
log-bin = /usr/local/mysql-5.7.35/logs/mysql-bin.log
binlog_format = mixed
sync_binlog = 5

lower_case_table_names=1
port = 3306
socket = /tmp/mysql.sock

basedir = /usr/local/mysql-5.7.35/
datadir = /usr/local/mysql-5.7.35/data
user = mysql
bind-address = 0.0.0.0
server-id = 1


init-connect = 'SET NAMES utf8mb4'
character-set-server = utf8mb4

#skip-name-resolve
#skip-networking
back_log = 300

max_connections = 1000
max_connect_errors = 6000
open_files_limit = 65535
table_open_cache = 128
max_allowed_packet = 4M
binlog_cache_size = 1M
max_heap_table_size = 8M
tmp_table_size = 16M

read_buffer_size = 2M
read_rnd_buffer_size = 8M
sort_buffer_size = 8M
join_buffer_size = 8M
key_buffer_size = 4M

thread_cache_size = 8

query_cache_type = 1
query_cache_size = 8M
query_cache_limit = 2M

ft_min_word_len = 4

log_bin = mysql-bin
binlog_format = mixed
expire_logs_days = 30

log_error = /usr/local/mysql-5.7.35/logs/mysql-error.log
slow_query_log = 1
long_query_time = 1
slow_query_log_file = /usr/local/mysql-5.7.35/logs/mysql-slow.log

performance_schema = 0
explicit_defaults_for_timestamp

#lower_case_table_names = 1

skip-external-locking

default_storage_engine = InnoDB
#default-storage-engine = MyISAM
innodb_file_per_table = 1
innodb_open_files = 500
innodb_buffer_pool_size = 64M
innodb_write_io_threads = 4
innodb_read_io_threads = 4
innodb_thread_concurrency = 0
innodb_purge_threads = 1
innodb_flush_log_at_trx_commit = 2
innodb_log_buffer_size = 2M
innodb_log_file_size = 32M
innodb_log_files_in_group = 3
innodb_max_dirty_pages_pct = 90
innodb_lock_wait_timeout = 120

bulk_insert_buffer_size = 8M
myisam_sort_buffer_size = 8M
myisam_max_sort_file_size = 10G
myisam_repair_threads = 1

interactive_timeout = 28800
wait_timeout = 28800

[mysqldump]
quick
max_allowed_packet = 16M

[myisamchk]
key_buffer_size = 8M
sort_buffer_size = 8M
read_buffer = 4M
write_buffer = 4M
[mysqld_safe]
log_error = /usr/local/mysql-5.7.35/logs/mysql-error.log
pid-file = /usr/local/mysql-5.7.35/logs/mysql.pid
```