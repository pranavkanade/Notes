# Notes

Day-to-day notes

```shell
# Add cronjobs
add_cronjob() {
    (crontab -l ; echo "*/5 * * * * /nz/support/bin/monitor.sh -type all -pmr 12345 -archive_plans YES >> /dev/null 2>&1") | sort - | uniq - | crontab -
}

add_cronjob
```

