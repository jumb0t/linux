# Увеличение максимального числа открытых файлов
fs.file-max = 2097152

# Оптимизация файловой системы
vm.swappiness = 10
vm.dirty_ratio = 15
vm.dirty_background_ratio = 5
vm.vfs_cache_pressure = 50
vm.overcommit_memory = 1
vm.overcommit_ratio = 100
vm.dirty_writeback_centisecs = 100

# Увеличение диапазона локальных портов
net.ipv4.ip_local_port_range = 1024 65535

# Оптимизация сетевых настроек
net.core.rmem_default = 262144
net.core.wmem_default = 262144
net.core.rmem_max = 134217728
net.core.wmem_max = 134217728
net.core.optmem_max = 134217728
net.core.netdev_max_backlog = 250000
net.core.somaxconn = 65535

# TCP настройки
net.ipv4.tcp_fastopen = 3
net.ipv4.tcp_mtu_probing = 1
net.ipv4.tcp_rmem = 4096 87380 134217728
net.ipv4.tcp_wmem = 4096 65536 134217728
net.ipv4.tcp_congestion_control = bbr
net.ipv4.tcp_keepalive_time = 600
net.ipv4.tcp_keepalive_intvl = 15
net.ipv4.tcp_keepalive_probes = 5
net.ipv4.tcp_fin_timeout = 15
net.ipv4.tcp_slow_start_after_idle = 0
net.ipv4.tcp_tw_reuse = 1
net.ipv4.tcp_max_syn_backlog = 8192
net.ipv4.tcp_syncookies = 1
net.ipv4.tcp_window_scaling = 1
net.ipv4.tcp_ecn = 1

# Очереди сигналов
kernel.pid_max = 4194303
kernel.threads-max = 999999
kernel.sched_migration_cost_ns = 5000000
kernel.sched_autogroup_enabled = 0

# Отключение IPv6 (если не используется)
net.ipv6.conf.all.disable_ipv6 = 1
net.ipv6.conf.default.disable_ipv6 = 1
net.ipv6.conf.lo.disable_ipv6 = 1

# Безопасность сети
net.ipv4.icmp_echo_ignore_all = 1
net.ipv4.icmp_echo_ignore_broadcasts = 1
net.ipv4.icmp_ignore_bogus_error_responses = 1
net.ipv4.ip_forward = 0
net.ipv4.conf.all.rp_filter = 1
net.ipv4.conf.default.rp_filter = 1
net.ipv4.conf.all.accept_source_route = 0
net.ipv4.conf.default.accept_source_route = 0
net.ipv4.conf.all.accept_redirects = 0
net.ipv4.conf.default.accept_redirects = 0
net.ipv4.conf.all.secure_redirects = 0
net.ipv4.conf.default.secure_redirects = 0
net.ipv4.conf.all.log_martians = 1
net.ipv4.conf.default.log_martians = 1

# Дополнительные настройки безопасности
kernel.randomize_va_space = 2
kernel.kptr_restrict = 2
kernel.dmesg_restrict = 1
kernel.perf_event_paranoid = 3
kernel.yama.ptrace_scope = 2
kernel.unprivileged_bpf_disabled = 1
user.max_user_namespaces = 0

# Оптимизация для SSD (если применимо)
vm.laptop_mode = 0

# Очереди приема и передачи
net.core.netdev_budget = 600
net.core.netdev_budget_usecs = 6000

# Планировщик пакетов
net.core.default_qdisc = fq



# Оптимизация управления памятью
vm.min_free_kbytes = 65536
vm.dirty_expire_centisecs = 200
vm.dirty_writeback_centisecs = 100
vm.dirty_background_bytes = 16777216  # 16MB
vm.dirty_bytes = 50331648             # 48MB
vm.zone_reclaim_mode = 0
vm.max_map_count = 262144

# Увеличение буферов для чтения и записи
net.core.optmem_max = 25165824
net.ipv4.udp_rmem_min = 163840
net.ipv4.udp_wmem_min = 163840

# Улучшение производительности TCP
net.ipv4.tcp_sack = 1
net.ipv4.tcp_timestamps = 1
net.ipv4.tcp_no_metrics_save = 1
net.ipv4.tcp_moderate_rcvbuf = 1
net.ipv4.tcp_rfc1337 = 1
net.ipv4.tcp_abort_on_overflow = 0
net.ipv4.tcp_syn_retries = 2
net.ipv4.tcp_synack_retries = 2
net.ipv4.tcp_max_orphans = 32768
net.ipv4.tcp_max_tw_buckets = 1440000

# Оптимизация сетевых параметров
net.nf_conntrack_max = 2621440
net.netfilter.nf_conntrack_max = 2621440
net.netfilter.nf_conntrack_tcp_timeout_established = 86400
net.ipv4.netfilter.ip_conntrack_max = 2621440

# Увеличение размера очереди соединений
net.core.netdev_max_backlog = 500000

# Оптимизация работы с дисками
vm.dirty_background_bytes = 16777216
vm.dirty_bytes = 50331648
vm.disk_writeback_centisecs = 100

# Повышение производительности NUMA (если применимо)
vm.zone_reclaim_mode = 0

# Оптимизация планировщика процессов
kernel.sched_latency_ns = 6000000
kernel.sched_min_granularity_ns = 750000
kernel.sched_wakeup_granularity_ns = 1000000
kernel.sched_migration_cost_ns = 500000

# Увеличение максимального числа соединений
net.core.somaxconn = 65535
net.ipv4.tcp_max_syn_backlog = 16384

# Снижение нагрузки на CPU от RCU (Read-Copy Update)
kernel.rcu_idle_gp_delay = 1

# Улучшение производительности для больших файлов
fs.nr_open = 1048576
fs.file-max = 2097152


# Сетевые оптимизации
net.core.dev_weight = 512
net.core.netdev_budget = 6000
net.core.netdev_budget_usecs = 12000
net.core.rps_sock_flow_entries = 32768
net.ipv4.tcp_max_orphans = 262144
net.ipv4.tcp_max_syn_backlog = 262144
net.core.netdev_max_backlog = 1000000
net.ipv4.tcp_low_latency = 1
net.ipv4.tcp_fin_timeout = 10
net.ipv4.ipfrag_high_thresh = 8388608
net.ipv4.ipfrag_low_thresh = 6291456

# Управление памятью
vm.swappiness = 1
vm.dirty_ratio = 15
vm.dirty_background_ratio = 5
vm.min_free_kbytes = 1048576
vm.max_map_count = 524288

# Файловая система и ввод-вывод
fs.file-max = 5242880
fs.nr_open = 2097152

# Планировщик процессов
kernel.sched_migration_cost_ns = 5000000
kernel.sched_autogroup_enabled = 1
kernel.sched_latency_ns = 6000000
kernel.sched_min_granularity_ns = 750000
kernel.sched_wakeup_granularity_ns = 1000000

# Системные лимиты
kernel.threads-max = 2097152

# Безопасность
kernel.randomize_va_space = 2
kernel.dmesg_restrict = 1

# Прочее
vm.stat_interval = 10
